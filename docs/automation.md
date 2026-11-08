# Repository automation

Every repository runs CI on pull requests targeting `main` and on pushes to `main`. Pull requests also run a review policy check. The workflows run with read-only tokens except for CodeQL results uploads and the existing deployment or release jobs that need specific write permissions.

## Checks by repository

| Repository | CI verification | Dependabot ecosystems |
| --- | --- | --- |
| Beatrice-website | Node 24 and `npm ci`, Oxlint, TypeScript and Vite build, Python helper syntax | npm, GitHub Actions |
| Dataset Web UI (macOS and Windows) | Lockfile-based frontend build with TypeScript. Python 3.12 unit and FastAPI integration tests with CPU PyTorch and isolated SQLite and output directories | npm in `/frontend`, pip in `/voiceforge-backend`, GitHub Actions |
| Trainer (macOS and Windows) | JavaScript, Python and shell syntax. Build the Python wheel from the existing Hatchling package | pip at the root, uv in `/beatrice-trainer`, GitHub Actions |
| Voice Changer (macOS) | JavaScript, Python and shell syntax. Build the Apple Silicon DMG with the existing bundled Python and ad-hoc signing workflow | npm, pip, GitHub Actions |
| Voice Changer (Windows) | JavaScript and Python syntax. Build the installer and portable archive on Windows using the existing package script | npm, pip, GitHub Actions |
| Beatrice-colab | Validate Colab and Kaggle notebook structure with nbformat | GitHub Actions |
| Beatrice-voice-models | Parse model metadata and check ZIP integrity and paths without extraction | GitHub Actions |
| Organization `.github` | Validate Actions workflow, issue form and Mergify schemas | GitHub Actions |

The dataset repositories have the existing runnable unit and integration suites. The Windows voice changer's DLL diagnostic requires a separately built DLL and only prints on failure. It receives syntax checking in CI. GPU training, live audio devices, VST3 loading and hosted notebook execution still need their target environments. The standalone Python helpers in the website and the installs inside notebook cells have no tracked dependency manifest. Review their dependencies when changing those files.

The website stays connected to Vercel. Its GitHub Pages workflow publishes the legacy redirect. The Windows voice changer still publishes release assets only when a maintainer dispatches its release workflow for a tag. The packaging job has read-only access and passes files to a separate release upload job.

## Dependency and code scanning

Dependabot checks each listed ecosystem weekly. It groups minor and patch version bumps, keeps major updates separate, and limits the number of open version PRs. Python application requirements without lockfiles retain their existing constraints. Review matching trainer changes in both `requirements.txt` and `beatrice-trainer/pyproject.toml` when a shared dependency moves. The Dependency review check rejects newly introduced high or critical advisories in dependency graphs for application repositories. Existing alerts should be triaged separately in the Security tab.

CodeQL detects supported languages and scans on pull requests, pushes to `main` and a staggered weekly schedule. It uses buildless extraction. The profile, notebook and model repositories are scanned for GitHub Actions workflow code. Notebook cells and binary model contents fall outside CodeQL source analysis. If a repository has CodeQL default setup enabled later, use only one setup to avoid duplicate analyses. Use the advanced workflow in this rollout.

## Pull request policy

The Reviewpad app is in maintenance mode and accepts no new installations. The organization has no existing installation. The **Review policy** job checks titles and descriptions on ready-for-review PRs and flags source changes without test changes and changes to sensitive files. The warnings prompt human review. The job has read-only pull request access. [Reviewpad app status](https://github.com/apps/reviewpad)

## Enable SonarQube analysis

SonarQube workflows are prepared for the website, dataset apps, trainers and voice changers. Each repository scopes its own application code and excludes build outputs, dependency directories and generated artifacts. The dataset test directories are classified as tests. The existing suites do not produce configured coverage reports, so these scans do not ingest coverage.

1. Import the GitHub repository into SonarQube Cloud or create a project on a supported SonarQube Server. Connect the GitHub integration if you want PR decoration. For Cloud CI scans, turn off automatic analysis in the Sonar project.
2. Under **Settings → Secrets and variables → Actions**, add a project-scoped analysis token as the Actions secret `SONAR_TOKEN`.
3. Add the Actions variable `SONAR_PROJECT_KEY`. For Cloud, also add `SONAR_ORGANIZATION`. For a server or a Cloud region using a different host, set `SONAR_HOST_URL` to the HTTPS URL the runner can reach. The default host is `https://sonarcloud.io`.
4. Set `SONAR_ENABLED=true` and dispatch **SonarQube** from `main` to verify the scan and quality gate. Set `SONAR_PR_ANALYSIS=true` only if your Sonar plan supports PR analysis and you want it for same-repository PRs. Fork and Dependabot PRs keep the standard CI, Dependency review and CodeQL checks.
5. After the quality gate has run, copy its badge from the Sonar project's Information page if desired. Keep the Sonar job optional unless the required check can be produced for every PR you accept.

For a server with a private CA, add its certificate according to the scanner action's setup instructions. [SonarQube scan action](https://github.com/SonarSource/sonarqube-scan-action)

## Enable Mergify after branch rules are in place

The checked-in Mergify rule ships disabled. It only targets a ready, up-to-date PR that changes exactly `README.md`, has the maintainer-applied `automerge:docs` label and an approval, has no outstanding change requests, and passes the repository's CI, CodeQL, Review policy and applicable Dependency review checks. Dependabot PRs are excluded and dependency manifests cannot match the file constraint.

1. Install the Mergify GitHub App on selected repositories only. Keep the app out of all protection bypass lists.
2. On `main`, require pull requests, at least one approving review, dismissal of stale approvals, and the successful checks listed in that repository's `.mergify.yml`. Enable squash merging. Confirm your existing protection settings and any additional required security checks.
3. Use Mergify's configuration validator, then enable the rule by removing its `disabled` block in a reviewed PR. Create the `automerge:docs` label and apply it only after inspecting the change.

Mergify inherits applicable GitHub branch protection and ruleset requirements. [Mergify merge action](https://docs.mergify.com/workflow/actions/merge/)

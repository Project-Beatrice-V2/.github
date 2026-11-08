# Contributing to Project Beatrice V2

Open the README in the repository you want to change and follow its platform and dependency setup. For projects with a Node lockfile, use `npm ci`. Keep dependency changes and their lockfile changes together.

Open pull requests against `main`. Give each PR a descriptive title and summarize the change, why it matters, and how you verified it. Use draft status while the work is in progress. For changes to application behavior, update the existing tests where practical. If the repository has no harness or the change needs audio hardware, record the platform, steps and result of your manual verification.

Keep generated installers, model weights, sample audio and credentials out of source changes unless the repository specifically manages those assets. Model contributions should follow the model repository's licensing and provenance requirements. Call out changes to dependencies, permissions, GitHub Actions, release scripts, launchers and bundled binaries in the PR so maintainers can review them closely.

Maintainers should review the diff and all applicable checks before merging. Report vulnerabilities privately as described in [SECURITY.md](SECURITY.md). See the [automation guide](docs/automation.md) for check coverage and maintainer setup.

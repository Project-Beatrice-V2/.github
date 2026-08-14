<div align="center">

  <!-- Animated Typing SVG Header -->
  <a href="https://github.com/Project-Beatrice-V2">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1000&color=F6AD55&center=true&vcenter=true&width=750&lines=%F0%9F%8E%99%EF%B8%8F+Project+Beatrice+V2;Next-Gen+Neural+Voice+Conversion;Sub-50ms+Ultra-Low+Latency+Inference;Local+Training+(macOS+%7C+Windows)+%2B+Colab;Dataset+Curation+Web+UI+Tools" alt="Project Beatrice V2 Typing Header" />
  </a>

  <br />

  <p align="center">
    <strong>An open-source, end-to-end neural voice conversion & model training ecosystem built for ultra-low latency, quality, and cross-platform flexibility.</strong>
  </p>

  <!-- Badges -->
  <p align="center">
    <a href="https://project-beatrice-v2.github.io/Beatrice-website/"><img src="https://img.shields.io/badge/Website-Visit_Official_Site-7C3AED?style=for-the-badge&logo=vercel&logoColor=white" alt="Official Website" /></a>
    <a href="https://github.com/Project-Beatrice-V2"><img src="https://img.shields.io/badge/Architecture-Beatrice_V2_Neural_Engine-7C3AED?style=for-the-badge&logo=cpu&logoColor=white" alt="Beatrice V2 Architecture" /></a>
    <a href="https://github.com/Project-Beatrice-V2"><img src="https://img.shields.io/badge/Platforms-macOS_%7C_Windows_%7C_Cloud-007ACC?style=for-the-badge&logo=apple&logoColor=white" alt="Platforms" /></a>
    <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-10B981?style=for-the-badge&logo=open-source-initiative&logoColor=white" alt="MIT License" /></a>
    <a href="https://github.com/Project-Beatrice-V2/Beatrice-voicechanger-macos"><img src="https://img.shields.io/badge/Latency-%3C_50ms_Real--time-EF4444?style=for-the-badge&logo=lightning&logoColor=white" alt="Low Latency" /></a>
  </p>

  <img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" alt="Animated Divider" />

</div>

<br />

## ⚡ The Beatrice V2 Pipeline

```
  ┌───────────────────────────┐      ┌───────────────────────────┐      ┌───────────────────────────┐
  │  1. Dataset Web UI        │ ───► │  2. Model Trainer         │ ───► │  3. Real-Time Changer     │
  │  • Audio Slicing & Clean  │      │  • macOS (MPS) & Win (CUDA│      │  • Ultra-low latency VST  │
  │  • Quality Validation     │      │  • Free Google Colab      │      │  • Live Discord/OBS stream│
  └───────────────────────────┘      └───────────────────────────┘      └───────────────────────────┘
```

<br />

## 📦 Repositories & Modules Directory

<table>
  <thead>
    <tr>
      <th width="32%">Module / Repository</th>
      <th width="22%">Platform Support</th>
      <th width="46%">Features & Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <a href="https://github.com/Project-Beatrice-V2/Beatrice-website">
          <strong>🌿 Beatrice-website</strong>
        </a>
      </td>
      <td><img src="https://img.shields.io/badge/Web-Live_Production-7C3AED?style=flat-square&logo=vercel&logoColor=white" alt="Web" /></td>
      <td>Official modern web portal, interactive audio showcase, documentation hub, and multi-lingual portal for Project Beatrice V2.</td>
    </tr>
    <tr>
      <td>
        <a href="https://github.com/Project-Beatrice-V2/Beatrice-voice-models">
          <strong>🎭 Beatrice-voice-models</strong>
        </a>
      </td>
      <td><img src="https://img.shields.io/badge/Cross--Platform-Model_Hub-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="Model Hub" /></td>
      <td>Official repository of pre-trained Beatrice neural voice weights and models (including Donald Trump 5,000-step checkpoint).</td>
    </tr>
    <tr>
      <td>
        <a href="https://github.com/Project-Beatrice-V2/Beatrice-voicechanger-macos">
          <strong>🎙️ Beatrice-voicechanger-macos</strong>
        </a>
      </td>
      <td><img src="https://img.shields.io/badge/macOS-Metal_MPS-000000?style=flat-square&logo=apple&logoColor=white" alt="macOS" /></td>
      <td>Real-time Beatrice voice changer for macOS featuring Metal/MPS hardware acceleration and ultra-low latency.</td>
    </tr>
    <tr>
      <td>
        <a href="https://github.com/Project-Beatrice-V2/Beatrice-voicechanger-windows">
          <strong>🎙️ Beatrice-voicechanger-windows</strong>
        </a>
      </td>
      <td><img src="https://img.shields.io/badge/Windows-CUDA_/_DirectML-0078D4?style=flat-square&logo=windows&logoColor=white" alt="Windows" /></td>
      <td>Fast, lightweight, low-latency live voice conversion running locally with GPU acceleration on Windows.</td>
    </tr>
    <tr>
      <td>
        <a href="https://github.com/Project-Beatrice-V2/Beatrice-trainer-macos">
          <strong>🧠 Beatrice-trainer-macos</strong>
        </a>
      </td>
      <td><img src="https://img.shields.io/badge/macOS-Metal_MPS-000000?style=flat-square&logo=apple&logoColor=white" alt="macOS" /></td>
      <td>Train Beatrice voice models locally on macOS with a clean desktop UI and optimized Apple Silicon pipeline.</td>
    </tr>
    <tr>
      <td>
        <a href="https://github.com/Project-Beatrice-V2/Beatrice-trainer-windows">
          <strong>🧠 Beatrice-trainer-windows</strong>
        </a>
      </td>
      <td><img src="https://img.shields.io/badge/Windows-CUDA-0078D4?style=flat-square&logo=windows&logoColor=white" alt="Windows" /></td>
      <td>Streamlined Windows trainer for custom voice models with complete offline support and efficient training.</td>
    </tr>
    <tr>
      <td>
        <a href="https://github.com/Project-Beatrice-V2/Beatrice-colab">
          <strong>☁️ Beatrice-colab</strong>
        </a>
      </td>
      <td><img src="https://img.shields.io/badge/Cloud-Colab_/_Kaggle-F9AB00?style=flat-square&logo=googlecolab&logoColor=white" alt="Colab" /></td>
      <td>Cloud training notebooks for Google Colab & Kaggle. Train models on free T4/A100 GPUs without local hardware.</td>
    </tr>
    <tr>
      <td>
        <a href="https://github.com/Project-Beatrice-V2/Beatrice-dataset-webui-macos">
          <strong>📂 Beatrice-dataset-webui-macos</strong>
        </a>
      </td>
      <td><img src="https://img.shields.io/badge/macOS-Web_UI-000000?style=flat-square&logo=apple&logoColor=white" alt="macOS" /></td>
      <td>Web-based dataset creator for macOS. Automatically slice long audio files, clean noise, and format training sets.</td>
    </tr>
    <tr>
      <td>
        <a href="https://github.com/Project-Beatrice-V2/Beatrice-dataset-webui-windows">
          <strong>📂 Beatrice-dataset-webui-windows</strong>
        </a>
      </td>
      <td><img src="https://img.shields.io/badge/Windows-Web_UI-0078D4?style=flat-square&logo=windows&logoColor=white" alt="Windows" /></td>
      <td>Intuitive web UI for Windows to build, process, and package voice datasets for Beatrice model training.</td>
    </tr>
  </tbody>
</table>

<br />

---

## 🛠️ End-to-End Workflow

<details open>
<summary><strong>Step 1: Dataset Preparation (Web UI)</strong></summary>
<br />

1. Launch **[Beatrice-dataset-webui-macos](https://github.com/Project-Beatrice-V2/Beatrice-dataset-webui-macos)** or **[Beatrice-dataset-webui-windows](https://github.com/Project-Beatrice-V2/Beatrice-dataset-webui-windows)** depending on your OS.
2. Load your raw voice recordings into the interface.
3. Automatically slice long files into clean audio segments, validate transcriptions/silence, and export a ready-to-train dataset zip.
</details>

<details>
<summary><strong>Step 2: Model Training</strong></summary>
<br />

* **macOS (Local):** Use **[Beatrice-trainer-macos](https://github.com/Project-Beatrice-V2/Beatrice-trainer-macos)** for native Apple Silicon MPS training.
* **Windows (Local):** Use **[Beatrice-trainer-windows](https://github.com/Project-Beatrice-V2/Beatrice-trainer-windows)** for CUDA / DirectML hardware acceleration.
* **Cloud (Free GPU):** Launch **[Beatrice-colab](https://github.com/Project-Beatrice-V2/Beatrice-colab)** on Google Colab or Kaggle to train without needing a high-end local GPU.
</details>

<details>
<summary><strong>Step 3: Real-Time Live Inference</strong></summary>
<br />

1. Download pre-trained weights from **[Beatrice-voice-models](https://github.com/Project-Beatrice-V2/Beatrice-voice-models)** or export your custom model.
2. Open **[Beatrice-voicechanger-macos](https://github.com/Project-Beatrice-V2/Beatrice-voicechanger-macos)** or **[Beatrice-voicechanger-windows](https://github.com/Project-Beatrice-V2/Beatrice-voicechanger-windows)**.
3. Route your physical microphone into the voice changer and output to a virtual audio channel (e.g. VB-Cable / BlackHole).
4. Use transformed voices live in Discord, OBS, games, or live streaming apps!
</details>

<br />

---

<div align="center">

  <img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" alt="Animated Divider" />

  <br />

  <sub>Built with ❤️ by the Project Beatrice V2 Team • Released under the MIT License</sub>

</div>

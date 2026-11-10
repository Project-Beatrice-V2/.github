<div align="center">

<img src="https://raw.githubusercontent.com/satiricalguru/Beatrice-voicechanger-mac/main/docs/media/app-icon.png" alt="Beatrice" width="112" />

# Project Beatrice

**Free, open-source, real-time AI voice changing. On your own computer.**<br/>
Change your voice live in Discord, Zoom, OBS and games, then train a voice of your own.

[![Website](https://img.shields.io/badge/Website-project--beatrice.vercel.app-7c8cff?style=for-the-badge&labelColor=000000)](https://project-beatrice.vercel.app)
[![Download for Mac](https://img.shields.io/github/v/release/satiricalguru/Beatrice-voicechanger-mac?style=for-the-badge&label=Mac&logo=apple&logoColor=white&color=000000&labelColor=000000)](https://github.com/satiricalguru/Beatrice-voicechanger-mac/releases/latest)
[![Download for Windows](https://img.shields.io/github/v/release/satiricalguru/Beatrice-voicechanger-windows?style=for-the-badge&label=Windows&logo=windows&logoColor=white&color=000000&labelColor=000000)](https://github.com/satiricalguru/Beatrice-voicechanger-windows/releases/latest)
[![Stars](https://img.shields.io/endpoint?url=https%3A%2F%2Fproject-beatrice.vercel.app%2Fapi%2Fstars%3Fformat%3Dshields&style=for-the-badge)](https://github.com/Project-Beatrice-V2)

<br/>

<a href="https://project-beatrice.vercel.app">
  <img src="https://raw.githubusercontent.com/Project-Beatrice-V2/Beatrice-website/main/docs/media/home.jpg" alt="Beatrice — Become any voice. In real time." width="100%" />
</a>

</div>

## ✨ What you get

- 🎙️ **Live voice changing, about 10 ms.** The Beatrice 2.0 neural engine runs on your machine. No cloud, no account, no subscription.
- 📦 **Download and go.** The Mac and Windows apps have everything inside, and set up the virtual microphone for you on first launch.
- 🎭 **112 voices built in.** Import more, or train your own from a few minutes of recordings.
- 🔊 **Soundboard and library.** 100+ meme and effect sounds with artwork, playable straight into your call.
- 🆓 **Open source.** MIT-licensed apps, made in the open.

## 🧭 Start here

| I want to… | Go to |
|:--|:--|
| **Change my voice on a Mac** (Apple Silicon) | [**Beatrice for Mac**](https://github.com/satiricalguru/Beatrice-voicechanger-mac) · [mirror](https://github.com/Project-Beatrice-V2/Beatrice-voicechanger-macos) |
| **Change my voice on Windows** 10/11 | [**Beatrice for Windows**](https://github.com/satiricalguru/Beatrice-voicechanger-windows) · [mirror](https://github.com/Project-Beatrice-V2/Beatrice-voicechanger-windows) |
| **Get more voices** | [Beatrice-voice-models](https://github.com/Project-Beatrice-V2/Beatrice-voice-models) |
| **Train my own voice** | [Trainer for Mac](https://github.com/Project-Beatrice-V2/Beatrice-trainer-macos) · [Trainer for Windows](https://github.com/Project-Beatrice-V2/Beatrice-trainer-windows) · [Colab & Kaggle](https://github.com/Project-Beatrice-V2/Beatrice-colab) |
| **Prepare recordings for training** | [Dataset Web UI for Mac](https://github.com/Project-Beatrice-V2/Beatrice-dataset-webui-macos) · [for Windows](https://github.com/Project-Beatrice-V2/Beatrice-dataset-webui-windows) |
| **Read guides, hear samples** | [project-beatrice.vercel.app](https://project-beatrice.vercel.app) · [website source](https://github.com/Project-Beatrice-V2/Beatrice-website) |

## 🛠️ From recordings to a live voice

```mermaid
flowchart LR
  rec([🎤 Your recordings]) --> ds[📂 Dataset Web UI<br/>slice · clean · check]
  ds --> train[🧠 Trainer<br/>Mac · Windows · Colab]
  hub[🎭 Voice models] --> app
  train --> app[🎙️ Voice changer<br/>Mac · Windows]
  app --> live([Discord · Zoom · OBS · games])
```

<details>
<summary><b>1 · Prepare a dataset</b></summary>
<br/>

Open the Dataset Web UI ([Mac](https://github.com/Project-Beatrice-V2/Beatrice-dataset-webui-macos) / [Windows](https://github.com/Project-Beatrice-V2/Beatrice-dataset-webui-windows)), load your recordings, and it slices them into clean clips and exports a ready-to-train dataset.
</details>

<details>
<summary><b>2 · Train a model</b></summary>
<br/>

Train locally with the trainer for [Mac](https://github.com/Project-Beatrice-V2/Beatrice-trainer-macos) (Apple Silicon) or [Windows](https://github.com/Project-Beatrice-V2/Beatrice-trainer-windows) (NVIDIA CUDA), or on a free cloud GPU with the [Colab & Kaggle notebooks](https://github.com/Project-Beatrice-V2/Beatrice-colab).
</details>

<details>
<summary><b>3 · Use it live</b></summary>
<br/>

In the voice changer, choose **Upload Custom Model** and pick your model's ZIP. Press the power button, pick the voice, and select the virtual microphone (BlackHole on Mac, VB-CABLE on Windows) in your call app.
</details>

<div align="center">
<br/>

<img src="https://raw.githubusercontent.com/satiricalguru/Beatrice-voicechanger-mac/main/docs/media/app-voices.jpg" alt="Beatrice voice models screen" width="49%" />
<img src="https://raw.githubusercontent.com/satiricalguru/Beatrice-voicechanger-mac/main/docs/media/app-soundboard.jpg" alt="Beatrice soundboard screen" width="49%" />

<br/><br/>

<sub>Built on the <a href="https://github.com/prj-beatrice/beatrice-vst">Beatrice engine</a> by prj-beatrice · Apps released under the MIT License · ⭐ Star a repo if Beatrice made you laugh</sub>

</div>

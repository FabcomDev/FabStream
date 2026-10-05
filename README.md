<!-- fabstream-page -->
<p align="center">
  <img src="assets/banner.png" alt="FabStream – 16:9 + 9:16 live at the same time" width="100%">
</p>

<p align="center">
  <a href="https://github.com/FabcomDev/FabStream/releases/latest/download/FabStream-Setup.exe"><img src="https://img.shields.io/badge/Download-Windows%2010%2F11-e3b866?style=for-the-badge&logo=windows&logoColor=0b0c10&labelColor=f3d79a" alt="Download for Windows"></a>
  <a href="https://fabstream.fabcom.workers.dev"><img src="https://img.shields.io/badge/Website-Premium%20%26%20Account-14161d?style=for-the-badge&labelColor=14161d&color=2a2d38" alt="Website"></a>
</p>

<p align="center">
  <a href="https://github.com/FabcomDev/FabStream/releases/latest"><img src="https://img.shields.io/github/v/release/FabcomDev/FabStream?style=flat-square&color=e3b866&labelColor=14161d&label=version" alt="Latest version"></a>
  <a href="https://github.com/FabcomDev/FabStream/releases"><img src="https://img.shields.io/github/downloads/FabcomDev/FabStream/total?style=flat-square&color=e3b866&labelColor=14161d" alt="Downloads"></a>
  <img src="https://img.shields.io/badge/price-free%20%2B%20Premium-e3b866?style=flat-square&labelColor=14161d" alt="Free + Premium">
  <img src="https://img.shields.io/badge/watermark-none-e3b866?style=flat-square&labelColor=14161d" alt="No watermark">
  <img src="https://img.shields.io/badge/output-up%20to%204K%20%C2%B7%20240%20fps-e3b866?style=flat-square&labelColor=14161d" alt="Up to 4K and 240 fps">
</p>

<h3 align="center">One project. Two independently designed outputs. Live and recorded at the same time.</h3>

<p align="center">
  FabStream is a dual-format broadcast studio for Windows: it streams <b>landscape (16:9)</b> to Twitch &amp; YouTube and <b>vertical (9:16)</b> live to TikTok<br>
  and other RTMP platforms <b>at the same time</b> – while recording ready-to-post 9:16 video for YouTube Shorts and Instagram Reels.<br>
  Each format has its own layout. No second PC, no cropping hacks, no cloud subscription.
</p>

<p align="center">
  <a href="#-new-in-13">New</a> ·
  <a href="#-why-fabstream">Features</a> ·
  <a href="#-how-it-works">How it works</a> ·
  <a href="#-platforms">Platforms</a> ·
  <a href="#-performance">Performance</a> ·
  <a href="#-free-vs-premium">Free vs. Premium</a> ·
  <a href="#%EF%B8%8F-install">Install</a> ·
  <a href="#-faq">FAQ</a> ·
  <a href="#-deutsch">Deutsch</a> ·
  <a href="CHANGELOG.md">Changelog</a>
</p>

<p align="center"><sub>Platform availability and RTMP access (for example a TikTok LIVE stream key) depend on your account and each platform's eligibility requirements.</sub></p>

---

## 🆕 New in 1.3

- **One encoder per format** – streaming, recording and the replay buffer of a format now share one encoder: everything in both formats runs on **2 encoder sessions** instead of 6.
- **Application audio** – Discord, Spotify or a game as its own mixer channel, or left out of the desktop audio.
- **Auto Moments** *(preview)* – loud reactions become "Save clip" suggestions while the replay buffer runs.
- **Up to 4K and 240 fps**, keyboard control everywhere (**F1** shows all shortcuts) and self-healing outputs.

All changes: [Changelog](CHANGELOG.md).

## ✨ Why FabStream

| | |
|---|---|
| 🖥️📱 **True dual output** | Two independent canvases. Place your camera, chat and overlays differently in 16:9 and 9:16; both go live with one click. |
| 🎛️ **Built for vertical** | Safe-zone overlays for TikTok, Shorts and Reels, copy a layout from the other format in one click, linked or separate positions per source. |
| ⚡ **One encoder per format** | Streaming, recording and the replay buffer of a format share one hardware encoder (NVIDIA NVENC, AMD AMF, Intel QSV, automatic x264 fallback). Everything in both formats needs just **2 encoder sessions**. |
| 📡 **Multistream** *(Premium)* | Send each format to up to 8 RTMP destinations at once: Twitch, YouTube, Kick, TikTok, Facebook, custom RTMP… If one platform drops, only that destination reconnects – the others keep running. |
| ⏪ **Replay buffer & instant clips** | Keeps the last minutes of both formats. One click (or hotkey) saves the moment as 16:9 **and** 9:16 MP4 – instantly, no re-encoding. |
| ✨ **Auto Moments** *(preview)* | A loud reaction on your mic or a big moment in the game sound becomes a "Save clip" suggestion (or is saved automatically). Only audio levels are analysed – nothing leaves your PC. |
| 🎧 **Application audio** | Record Discord, Spotify or a game as its own mixer channel with volume, mute and filters – or leave a program out of the desktop audio entirely. |
| 🎬 **Record while live** | Local recording of both formats in parallel to streaming, up to 4K and 240 fps. |
| 🎨 **Filters & mixer** | GPU video filters (chroma key, color, blur, crop…), microphones, desktop and application audio, audio filters. |
| 🩺 **Self-healing outputs** | A crashed encoder restarts on its own (recordings continue in a second file), destinations reconnect, and the Outputs panel warns early about an overloaded encoder, dropped frames or a slow upload. |
| ⌨️ **Keyboard first** | Esc = back, Enter = accept, Delete removes the selected scene or source, F2 rename, Ctrl+1…9 switch scenes, global hotkeys for going live and saving clips – **F1** shows them all. |
| 🔒 **Private by design** | Stream keys are stored encrypted with Windows DPAPI. No account needed for the free version, no telemetry. |

## 📸 Screenshots

<p align="center">
  <img src="assets/app-dual.png" alt="FabStream dual view: landscape and vertical canvas side by side" width="100%">
</p>
<p align="center"><sub>Dual view: the same scene, laid out separately for 16:9 and 9:16.</sub></p>

<p align="center">
  <img src="assets/app-context-menu.png" alt="FabStream editor with context menu" width="100%">
</p>
<p align="center"><sub>Snapping editor with per-format transforms, crop, fit/fill and quick actions.</sub></p>

## 🧭 How it works

1. **Build your scene once** – add your screen or a game window, webcam, images, video, text and audio.
2. **Lay it out twice** – arrange the 16:9 canvas for Twitch/YouTube and the 9:16 canvas for TikTok/Shorts. Sources can share a position or have their own per format.
3. **Go live** – each format streams to its own platforms, records locally and keeps a replay buffer. Save a clip at any moment and get both formats instantly.

<details>
<summary><b>⌨️ Keyboard shortcuts</b></summary>

| Keys | Action |
|---|---|
| <kbd>Esc</kbd> | Back: close the dialog or menu, otherwise deselect |
| <kbd>Enter</kbd> | Accept the dialog (OK, Save, Delete …) |
| <kbd>Ctrl</kbd>+<kbd>1</kbd> … <kbd>9</kbd> | Switch to scene 1 … 9 |
| <kbd>Ctrl</kbd>+<kbd>N</kbd> | New scene |
| <kbd>Ctrl</kbd>+<kbd>,</kbd> | Settings |
| <kbd>Delete</kbd> | Delete the selected scene or remove the selected source |
| <kbd>F2</kbd> | Rename the selected scene or source |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>D</kbd> | Duplicate the source |
| Arrow keys | Move the source 1 px (with <kbd>Shift</kbd> 10 px) |
| <kbd>Ctrl</kbd>+<kbd>F</kbd> / <kbd>Ctrl</kbd>+<kbd>S</kbd> / <kbd>Ctrl</kbd>+<kbd>D</kbd> | Fit / stretch / center on the canvas |
| <kbd>F1</kbd> | Show all shortcuts in the app |

Global hotkeys for going live, recording and saving clips work while you are in a game – set them in **Settings → Hotkeys**.
</details>

## 📡 Platforms

Each format streams to its own list of destinations – for example 16:9 to Twitch and YouTube, 9:16 to TikTok LIVE.

| Platform | How to connect |
|---|---|
| **Twitch** | built-in server, paste your stream key |
| **YouTube** | built-in server, paste your stream key (landscape or vertical live) |
| **TikTok LIVE** | paste the server URL and stream key from TikTok LIVE Producer\* |
| **Kick**, **Facebook**, **Instagram** | paste the RTMP(S) server URL and stream key the platform shows you\* |
| **Any other service** | every RTMP / RTMPS server (Restream, your own server, …) |

<sub>\* Platforms decide who gets a stream key; requirements (for example a minimum follower count for TikTok LIVE) vary by account and region.</sub>

## 🚀 Performance

Measured with FabStream's built-in benchmark on a Ryzen 7 7800X3D + GeForce RTX 5070 Ti (NVENC), 1080p60 in **both** formats at the same time:

| Scenario | Outputs | Encoder sessions | Render | Encoder speed | Dropped frames |
|---|:---:|:---:|:---:|:---:|:---:|
| Stream + recording, 16:9 + 9:16 | 4 | 2 | 60 fps | ≥ 1.01× | 0 |
| + replay buffer in both formats | 6 | 2 | 60 fps | ≥ 1.01× | 0 |

Compositing both canvases took about 0.2 ms per frame. Results on other hardware differ; the Outputs panel shows encoder speed and dropped frames live while you stream.

## 💎 Free vs. Premium

| | **Free** | **Premium** |
|---|:---:|:---:|
| 16:9 + 9:16 at the same time | ✅ | ✅ |
| Recording (both formats) | ✅ | ✅ |
| Output resolution | up to 1080p | **up to 4K** |
| Frame rate | up to 60 fps | **up to 240 fps** |
| Replay buffer & instant clips | last 2 min | **last 10 min** |
| Application audio (Discord, Spotify …) | ✅ | ✅ |
| Filters, hardware encoding, safe zones | ✅ | ✅ |
| Watermark | **none** | **none** |
| Platforms per format | 1 | **up to 8** |
| Platforms in total | 2 | **16** |
| PCs per license | 1 | **3** |
| Priority support | – | ✅ |
| Price | **0 €** | **6.99 € / month** or **59 € / year** |

Try Premium **7 days for free** inside the app (no credit card). Premium is purchased on the [FabStream website](https://fabstream.fabcom.workers.dev); your license key arrives by e-mail.

## ⬇️ Install

1. **[Download `FabStream-Setup.exe`](https://github.com/FabcomDev/FabStream/releases/latest/download/FabStream-Setup.exe)** (Windows 10/11, 64-bit).
2. Run it. If Windows SmartScreen shows *"Windows protected your PC"*: click **More info → Run anyway**.<br>
   <sub>FabStream is new and not yet known to SmartScreen; this message disappears as more people use it.</sub>
3. The setup assistant detects your GPU, picks the best encoder and helps you add your first platform.

FabStream checks for updates on every start. **Update & restart** downloads the new version, verifies its signature and checksum and installs it – your scenes and settings are kept.

| Requirements | |
|---|---|
| System | Windows 10 or 11 (64-bit) |
| Memory | 8 GB RAM (16 GB recommended for 1440p/4K) |
| Graphics | a GPU with H.264 hardware encoding recommended (NVIDIA GTX 10-series or newer, AMD RX 400 or newer, Intel 6th gen or newer) |
| Upload | ≈ 6 Mbit/s per destination at 1080p60 |

## ❓ FAQ

<details>
<summary><b>Is the free version really free?</b></summary>

Yes. Dual output (16:9 + 9:16 at once) up to 1080p60, recording, replay clips, application audio and all filters are free, with no watermark and no time limit. Premium adds streaming each format to several platforms at once, 1440p/4K, up to 240 fps and a 10-minute replay buffer.
</details>

<details>
<summary><b>Can FabStream replace OBS or Streamlabs?</b></summary>

If your focus is streaming and recording – and especially landscape + vertical at the same time – it can: both formats, multistream, replay clips and per-app audio are built in, without plugins. Workflows that depend on plugins, browser sources, scripting, a studio mode or a virtual camera may still need OBS.
</details>

<details>
<summary><b>Do I need a powerful PC for two formats?</b></summary>

Less than you might think: each format has exactly one encoder, no matter how many platforms you stream to, and the encoding runs on the graphics card. A current mid-range GPU handles both formats at 1080p60 with streaming, recording and the replay buffer. The Outputs panel warns you if your PC or upload cannot keep up.
</details>

<details>
<summary><b>Can I record Discord separately – or not at all?</b></summary>

Yes. Audio Mixer → Add Audio → <b>Application Audio</b> records one program as its own channel with its own volume. In the desktop audio settings you can also leave a program out completely.
</details>

<details>
<summary><b>Where do I enter my license key?</b></summary>

In FabStream: <b>Settings → Account → License key</b>. Lost it? Use "Lost your key?" in the same place, or the account page on the <a href="https://fabstream.fabcom.workers.dev">website</a>; it is sent to your purchase e-mail.
</details>

<details>
<summary><b>Can I stream vertical to TikTok and landscape to Twitch at the same time?</b></summary>

Yes – that is what FabStream is built for. Each format has its own layout and its own destinations, and both go live with one click. You need a TikTok LIVE stream key (see <a href="#-platforms">Platforms</a>).
</details>

<details>
<summary><b>Can I use FabStream only for recording, without streaming?</b></summary>

Yes. Record both formats as MP4 (or only one), keep a replay buffer and save clips – no platform account needed.
</details>

<details>
<summary><b>Is my stream key safe?</b></summary>

Stream keys never leave your PC except to the platform you stream to. They are stored encrypted with Windows DPAPI.
</details>

## 🔐 Verify your download

Every release lists the **SHA-256** checksum of `FabStream-Setup.exe` in its release notes and in `SHA256SUMS.txt` (signed: `SHA256SUMS.txt.sig`, see [SECURITY.md](SECURITY.md)). To check the file you downloaded, open PowerShell in your Downloads folder:

```powershell
Get-FileHash .\FabStream-Setup.exe -Algorithm SHA256
```

The hash must match the one in the [release notes](https://github.com/FabcomDev/FabStream/releases/latest).

## 📄 Documents

[Changelog](CHANGELOG.md) · [Security](SECURITY.md) · [Privacy policy](PRIVACY.md) · [End-user license (EULA)](EULA.md) · [Third-party licenses](THIRD_PARTY_NOTICES.md)

## 🇩🇪 Deutsch

<details>
<summary><b>FabStream auf Deutsch – kurz erklärt</b></summary>

FabStream ist ein Streaming-Studio für Windows, das **16:9 und 9:16 gleichzeitig** live sendet und aufnimmt – z. B. querformatig auf Twitch/YouTube und hochformatig auf TikTok LIVE, mit eigenem Layout pro Format.

- **Kostenlos:** beide Formate gleichzeitig bis 1080p60, Aufnahme, Replay-Clips (2 Minuten), Anwendungs-Audio (z. B. Discord separat), alle Filter – **ohne Wasserzeichen, ohne Zeitlimit**.
- **Premium (6,99 € / Monat oder 59 € / Jahr):** Multistream auf bis zu 8 Plattformen pro Format, bis 4K und 240 fps, 10 Minuten Replay-Puffer, 3 PCs pro Lizenz. 7 Tage gratis testen, ohne Kreditkarte.
- **Installation:** [`FabStream-Setup.exe` herunterladen](https://github.com/FabcomDev/FabStream/releases/latest/download/FabStream-Setup.exe) und starten. Zeigt Windows SmartScreen *„Der Computer wurde durch Windows geschützt"*: **Weitere Informationen → Trotzdem ausführen**.
- **Tastatur:** Esc = zurück, Enter = bestätigen, Entf löscht die gewählte Szene oder Quelle, **F1** zeigt alle Kürzel.

Premium, Konto und Lizenzschlüssel: [Website](https://fabstream.fabcom.workers.dev) (auch auf Deutsch).
</details>

## 💬 Support

Bugs, ideas and questions: open an [issue](https://github.com/FabcomDev/FabStream/issues). Premium and license questions: [website](https://fabstream.fabcom.workers.dev).

---

<p align="center">
  <sub><b>FabStream</b> is a project by <b>Fabcom</b>.<br>
  This repository hosts the official Windows downloads. FabStream is proprietary software (EULA shown during installation).<br>
  Third-party components (Electron – MIT, FFmpeg – GPL v3) are listed in <code>THIRD_PARTY_NOTICES.md</code> in the installation folder.<br>
  Twitch, YouTube, TikTok, Kick, Instagram and Facebook are trademarks of their respective owners; FabStream is not affiliated with them.</sub>
</p>

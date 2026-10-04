<!-- fabstream-page: managed by tools/release/release-github.mjs (source: github-page/README.md) -->
<p align="center">
  <img src="assets/banner.png" alt="FabStream – 16:9 + 9:16 live at the same time" width="100%">
</p>

<p align="center">
  <a href="https://github.com/FabcomDev/FabStream/releases/latest/download/FabStream-Setup.exe"><img src="https://img.shields.io/badge/Download-Windows%2010%2F11-e3b866?style=for-the-badge&logo=windows&logoColor=0b0c10&labelColor=f3d79a" alt="Download for Windows"></a>
</p>

<p align="center">
  <a href="https://github.com/FabcomDev/FabStream/releases/latest"><img src="https://img.shields.io/github/v/release/FabcomDev/FabStream?style=flat-square&color=e3b866&labelColor=14161d&label=version" alt="Latest version"></a>
  <a href="https://github.com/FabcomDev/FabStream/releases"><img src="https://img.shields.io/github/downloads/FabcomDev/FabStream/total?style=flat-square&color=e3b866&labelColor=14161d" alt="Downloads"></a>
  <img src="https://img.shields.io/badge/price-free%20%2B%20Premium-e3b866?style=flat-square&labelColor=14161d" alt="Free + Premium">
  <img src="https://img.shields.io/badge/watermark-none-e3b866?style=flat-square&labelColor=14161d" alt="No watermark">
</p>

<h3 align="center">One PC. Two formats. Every platform.</h3>

<p align="center">
  FabStream streams and records <b>landscape (16:9)</b> for Twitch &amp; YouTube and <b>vertical (9:16)</b> for TikTok, Shorts &amp; Reels <b>at the same time</b>,<br>
  each with its own layout. No second PC, no cropping hacks, no cloud subscription needed.
</p>

---

## ✨ Why FabStream

| | |
|---|---|
| 🖥️📱 **True dual output** | Two independent canvases. Place your camera, chat and overlays differently in 16:9 and 9:16; both go live from one click. |
| 🎛️ **Built for vertical** | TikTok / Shorts / Reels safe zones, one click to copy a layout from the other format, linked or separate positions per source. |
| ⚡ **Hardware encoding** | NVIDIA NVENC, AMD AMF and Intel QSV, with automatic x264 fallback. |
| 📡 **Multistream** *(Premium)* | Send each format to up to 8 platforms at once: Twitch, YouTube, Kick, TikTok, Facebook, custom RTMP… |
| 🎬 **Record while live** | Local recording of both formats in parallel to streaming. Ready-made clips for your shorts. |
| 🎨 **Filters & audio** | GPU video filters (chroma key, color, blur, crop…), mic + desktop audio, audio filters, mixer. |
| 🔁 **Auto-reconnect** | Dropped connection? FabStream reconnects each destination on its own. |
| 🔒 **Private by design** | Stream keys are stored encrypted with Windows DPAPI. No account needed to use the free version. |

## 📸 Screenshots

<p align="center">
  <img src="assets/app-dual.png" alt="FabStream dual view: landscape and vertical canvas side by side" width="100%">
</p>
<p align="center"><sub>Dual view: the same scene, laid out separately for 16:9 and 9:16.</sub></p>

<p align="center">
  <img src="assets/app-context-menu.png" alt="FabStream editor with context menu" width="100%">
</p>
<p align="center"><sub>Snapping editor with per-format transforms, crop, fit/fill and quick actions.</sub></p>

## 💎 Free vs. Premium

| | **Free** | **Premium** |
|---|:---:|:---:|
| 16:9 + 9:16 at the same time | ✅ | ✅ |
| Recording (both formats) | ✅ | ✅ |
| Filters, hardware encoding, safe zones | ✅ | ✅ |
| Watermark | **none** | **none** |
| Platforms per format | 1 | **up to 8** |
| Platforms in total | 2 | **16** |
| PCs per license | 1 | **3** |
| Priority support | – | ✅ |
| Price | **0 €** | **6.99 € / month** or **59 € / year** |

Try Premium **7 days for free** inside the app (no credit card). Premium is purchased on the FabStream website; your license key arrives by e-mail.

## ⬇️ Install

1. **[Download `FabStream-Setup.exe`](https://github.com/FabcomDev/FabStream/releases/latest/download/FabStream-Setup.exe)** (Windows 10/11, 64-bit).
2. Run it. If Windows SmartScreen shows *"Windows protected your PC"*: click **More info → Run anyway**.<br>
   <sub>FabStream is new and not yet known to SmartScreen; this message disappears as more people use it.</sub>
3. The setup assistant detects your GPU, picks the best encoder and helps you add your first platform.

FabStream checks for updates on start and tells you when a new version is available.

**Requirements:** Windows 10 or 11 (64-bit) · 8 GB RAM · a GPU with H.264 encoding recommended · for multistream: enough upload bandwidth for every destination (≈ 6 Mbit/s each at 1080p).

## ❓ FAQ

<details>
<summary><b>Is the free version really free?</b></summary>

Yes. Dual output (16:9 + 9:16 at once), recording and all filters are free, with no watermark and no time limit. Premium only adds streaming each format to several platforms at once.
</details>

<details>
<summary><b>Does it replace OBS / Streamlabs?</b></summary>

For most streamers, yes: scenes, sources, filters, audio mixer, recording and streaming. The difference: FabStream is built around running a landscape and a vertical stream at the same time.
</details>

<details>
<summary><b>Where do I enter my license key?</b></summary>

In FabStream: <b>Settings → Account → License key</b>. Lost it? Use "Lost your key?" in the same place; it is sent to your purchase e-mail.
</details>

<details>
<summary><b>Is my stream key safe?</b></summary>

Stream keys never leave your PC except to the platform you stream to. They are stored encrypted with Windows DPAPI.
</details>

## 💬 Support

Bugs, ideas and questions: open an [issue](https://github.com/FabcomDev/FabStream/issues).

---

<p align="center">
  <sub><b>FabStream</b> is a project by <b>Fabcom</b>.<br>
  This repository hosts the official Windows downloads. FabStream is proprietary software (EULA shown during installation).<br>
  Third-party components (Electron – MIT, FFmpeg – GPL v3) are listed in <code>THIRD_PARTY_NOTICES.md</code> in the installation folder.<br>
  Twitch, YouTube, TikTok, Kick, Instagram and Facebook are trademarks of their respective owners; FabStream is not affiliated with them.</sub>
</p>

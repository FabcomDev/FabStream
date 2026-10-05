# Changelog

All notable changes to FabStream. Each release on GitHub shows the section of its version.
Format: Added / Improved / Fixed / Known issues.

## 1.7.0 – 2026-10-05

### Improved
- 

## 1.6.0 – 2026-10-05

### Added
- **Sign in with Kick** (next to Twitch and TikTok, which are listed first) – and **connect Kick for streaming**: fetch your Kick stream key into a destination and set the stream title and category from Settings → Stream, like with Twitch.
- **Profile button** at the bottom right: your account, plan with **Upgrade**, Plan & license, Settings, report a bug, suggest an idea, sign in / out.

### Improved
- **Cleaner layout:** the title bar only shows FabStream. New scenes and sources are added with the `+` of the Scenes and Sources panels, **Record** and **Go Live** (all formats) are in the Outputs & Streaming panel.
- **Your plan decides what you can choose:** options of bigger plans (frame rate, resolution, replay length, more platforms per format, preview features) are shown with a 🔒 and the plan name but cannot be selected. When a trial ends or a plan changes, settings outside the plan are adjusted automatically – extra destinations are only switched off, never deleted.

### Removed
- **Steam sign-in.** Accounts that used Steam sign in with an e-mail code (or another linked sign-in) instead.

## 1.5.0 – 2026-10-05

### Added
- Website: home page links to the FabStream Product Hunt page (self-hosted badge – no third-party image or tracking).
- **FabStream account (optional).** Sign in with an e-mail code (no password) or with Twitch, Steam, TikTok, Discord or Google/YouTube – Settings → Account.
  - **Your plan on every PC:** plans bought with your account's e-mail address (or added with their key) work on any PC you sign in on – no license key to copy. Signing out frees the PC.
  - **Cloud sync:** upload scenes, sources and settings and load them on another PC. Stream keys never leave your PC.
  - **Twitch:** connect Twitch once, then fetch your stream key into a destination and change the stream title and category from Settings → Stream.
  - Manage everything in one place: linked sign-ins, signed-in devices, PCs per license, invoices & billing, delete account.
- **Report a bug / suggest an idea** right from Settings (bug and light-bulb buttons). Attach a log excerpt (stream keys and tokens are removed automatically), system info and a screenshot – only what you tick is sent.
- **Settings → Advanced:** turn the update check on start on or off, detailed (debug) logging, save and load a backup file of scenes + settings (never contains stream keys), and reset all settings to their defaults.
- **Scene transitions** on both formats at once: Cut, Fade, Fade to colour, Slide, Swipe, Wipe and **Stinger** (your own video, WebM with transparency or MP4, with sound and an adjustable switch point; optionally a separate 9:16 clip). Pick the default with the new transition button above the previews; any scene can have its own transition (scene menu → "Transition into this scene…"). Sound of video files fades along with the picture.
- **Studio mode:** prepare a scene in the preview while viewers keep seeing the live scene, then send it live with **Transition** (or **Cut**). Program and preview are shown for 16:9 and 9:16. Hotkeys for "send preview live" and "studio mode on/off" in Settings → Hotkeys. Leaving studio mode never changes what is live; the live scene cannot be deleted by accident.

### Improved
- Video files in scenes that are not live are now silent (before, their sound kept playing for a few seconds after switching away).

## 1.4.0 – 2026-10-05

### Added
- **Four plans: Free, Premium, Ultra and Max.**
  - Free: 16:9 + 9:16 at once, 1 platform per format, 1080p60, 2-minute replay buffer.
  - Premium ($4.99 / 4,99 € a month): 3 platforms per format, 1440p and 120 fps, 5-minute replay buffer, 1 PC.
  - Ultra ($9.99 / 9,99 €): 8 platforms per format, 4K and 240 fps, 10-minute replay buffer, 3 PCs.
  - Max ($19.99 / 19,99 €): everything in Ultra, 30-minute replay buffer, 5 PCs, early access to preview features (Auto Moments) and priority support.
  - Yearly plans: 2 months free.
- The upgrade dialog shows all plans side by side and recommends the plan a feature needs; settings mark options with the plan they need ("· Ultra").
- The 7-day trial now unlocks everything (Max).
- Website: four plan cards with prices in US$ (English) and € (German).

### Fixed
- **Website address:** the website, your account and license checks now run on https://fabstream.fabcom-dev.workers.dev (1.3.1 pointed to an address that is not in use). Please update.

## 1.3.1 – 2026-10-05

### Fixed
- **New website address:** FabStream now uses https://fabstream.fabcom.workers.dev for Premium, your account and license checks. Please update – version 1.3.0 still points to the old address.
- **Recordings and clips are never overwritten:** two recordings or clips started in the same second get separate files (`_2`, `_3` …).
- **Update download:** a full disk, missing write access or a dropped connection now ends the download at once with a clear message (before, it could hang).
- **Long replay sessions:** the replay buffer's segment list stays small however long you stream, and segments a clip is being cut from are kept until the clip is done.
- **Security:** FabStream only loads image and video files you chose yourself (network shares only when picked explicitly).
- **License server:** a PC limit can no longer be exceeded by activating several PCs at the same moment; late or repeated payment notifications can no longer switch a subscription back to an older state; only FabStream purchases (in the right test/live mode) create license keys; a license e-mail that could not be sent is sent again automatically; checkout attempts are rate limited.

### Improved
- **Website:** English by default, German for visitors from Germany, Austria, Switzerland and Liechtenstein; the EN/DE switch remembers your choice.
- **GitHub page:** what's new, supported platforms, keyboard shortcuts, more FAQ and a German summary.
- **Builds:** every release is compiled fresh from the source, runs the app and license-server tests and the self-test, and uses a locked FFmpeg build; each package records exactly what it contains (`build-info.json`).

## 1.3.0 – 2026-10-05

### Added
- **One encoder per format:** recording, every stream destination and the replay buffer of a format now share ONE encoder (before: one per output). Streaming + recording + replay buffer in 16:9 and 9:16 needs 2 encoder sessions instead of 6 – much less GPU load, no NVENC session limit problems.
- **Application audio:** Audio Mixer → Add Audio → *Application Audio* records a single program – e.g. Discord, Spotify or a game – as its own channel with volume, mute and filters. FabStream lists the programs that are playing sound; programs that are not running yet are picked up automatically when they start (and again after a restart).
- **Desktop Audio → Leave out application:** keep one program (e.g. Discord) out of the desktop mix – so it is not recorded at all, or only through its own fader. Adding an application channel does this automatically, so nothing is recorded twice.
- **Auto Moments (preview):** while the replay buffer runs, a loud reaction on your microphone or a loud moment in the game sound becomes a suggestion card with "Save clip" (or is saved automatically, max. 12 per hour). Settings → Replay & Clips → Auto Moments. Only levels are analysed, nothing leaves your PC; every suggestion is on the session timeline.
- **Keyboard control:** Esc = back (closes dialogs and menus, deselects), Enter = accept (OK / Save / Delete), Delete removes the clicked scene or source (with confirmation), arrows switch scenes / layers or nudge the source, F2 rename, Ctrl+N new scene, Ctrl+1…9 switch scene, Ctrl+Shift+D duplicate, Ctrl+, settings, arrow keys in menus. **F1** shows all shortcuts.
- **More video options:** output resolutions from 640×360 up to **4K** (3840×2160 / 2160×3840) and frame rates up to **240 fps**. FabStream now renders each format at exactly the output resolution – 1440p/4K are real, not upscaled, and smaller outputs cost less GPU.
- **BENCHMARK.cmd:** measures FabStream on your PC (stream + recording + replay in both formats at 1080p60) and writes a short report.
- **Output health** in the Outputs panel: warns when the encoder is overloaded, frames are dropped, the upload or the disk is too slow, or a destination reconnects.

### Improved
- **Multistream:** if one platform drops, only that destination reconnects – the others keep streaming without interruption.
- **Encoder supervision:** an encoder that crashes is restarted automatically (max. 3 times in 5 minutes); recordings continue in a second file (`…_part2`), streams re-publish.
- Recordings started while streaming begin immediately (from the last keyframe) instead of starting a second encoder.
- **Plans updated:** Free covers dual output, recording, replay clips (last 2 min), application audio and everything else up to 1080p at 60 fps. Premium adds multistream, 1440p/4K, up to 240 fps and a 10-minute replay buffer. Premium options are marked in the settings; starting them on Free opens the upgrade dialog.

### Fixed
- Application audio finds the right program after restarts (process ids are re-used by Windows; Discord's parent process exits) and only in your own Windows session; a game started as administrator is re-attached after it restarts.
- Desktop audio: unplugging the only headset shows "reconnecting" instead of staying "live", without filling the log every second.
- FabStream no longer shows up as an audio application (Windows volume mixer, Application Audio list): its mixer runs without opening a playback device.

## 1.2.0 – 2026-10-04

### Added
- **Replay buffer & instant clips:** keeps the last 30 s – 10 min of both formats; **Save clip** (button or Ctrl+Shift+C) writes the moment as MP4 – 16:9 and 9:16 at once, instantly, without re-encoding. Configurable seconds before/after.
- **Mark moment** (Ctrl+Shift+M) and a session timeline per stream (events and moments as JSONL next to your recordings).
- **Clip library:** play, show in folder, delete to the recycle bin; Highlight Score per clip.
- Settings → Replay & Clips; Diagnostics → Features (feature flags) and Advanced diagnostics.
- Settings → Audio → **Desktop audio capture**: Automatic (recommended) / all apps except FabStream / default playback device / legacy.

### Improved
- Buttons in the Outputs panel no longer miss clicks while live statistics update.

### Fixed
- **Desktop audio with headsets and when switching the sound output:** desktop audio is now captured by FabStream's own Windows audio helper. It works with devices Chromium could not open (Logitech G HUB 7.1, DualSense …), keeps running when you switch speakers ↔ headset, re-connects after a device is unplugged, and no longer records FabStream's own monitoring sound. The old capture path remains as an automatic fallback and now re-connects after a device switch too.

### Security
- The app UI can no longer open files directly (folders only); clips open through a checked path.

## 1.1.0 – 2026-10-04

### Added
- Settings → General: confirm before stopping, record automatically when going live, keep the PC awake while live, start with Windows.
- Settings → Hotkeys: start/stop streaming and recording, next/previous scene, mute microphones/desktop audio – in-app or global (also while gaming), with conflict messages.
- Settings → Advanced: process priority for FabStream and its encoders.
- Encoder: CBR/VBR rate control and H.264 profile. Stream: reconnect on/off, attempts and delay. Recording: file name prefix.
- In-app updates: FabStream checks GitHub on every start; "Update & restart" downloads the new version, verifies the Ed25519-signed checksum and the SHA-256, installs it and restarts FabStream.
- Release notes with SHA-256, signed `SHA256SUMS.txt`, SECURITY.md.

### Improved
- Desktop audio: clear message when Windows cannot capture the playback device; audio sources restart automatically when devices change.

### Known issues
- The installer is not code-signed yet: Windows SmartScreen asks for confirmation, and Windows 11 Smart App Control blocks it. The Microsoft Store version is signed by Microsoft.
- Desktop audio is captured from the Windows default playback device; some devices (e.g. game-controller headsets) cannot be captured – choose another output device.
- Multistream sends each destination from your PC, so it needs upload bandwidth for every destination.

## 1.0.0 – 2026-10-04

### Added
- Dual-format studio: one project, two independently designed canvases (16:9 and 9:16), streamed and recorded at the same time.
- Free plan: dual output (one platform per format), recording of both formats, all filters, no watermark, no time limit.
- Premium (optional subscription, 7-day trial in the app): multistream to up to 8 RTMP destinations per format, 3 PCs.
- Hardware encoding (NVIDIA NVENC, AMD AMF, Intel Quick Sync) with automatic x264 fallback.
- Safe-zone overlays for TikTok, Shorts and Reels; GPU video filters; audio mixer with filters.
- Update notice when a new version is published (no automatic download or installation).

### Known issues
- The installer is not code-signed yet: Windows SmartScreen asks for confirmation, and Windows 11 Smart App Control blocks it. The Microsoft Store version is signed by Microsoft.
- Multistream sends each destination from your PC, so it needs upload bandwidth for every destination.

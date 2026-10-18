# Third-Party Notices

FabStream bundles the following third-party software. Each component remains under its own license.

## Electron (MIT License)
Copyright (c) Electron contributors, Copyright (c) 2013-2020 GitHub Inc.
Electron includes Chromium and Node.js; their licenses are shipped as `LICENSE` and
`LICENSES.chromium.html` in the application folder. Source: https://github.com/electron/electron

## FFmpeg (GNU General Public License v3)
FabStream runs `resources\ffmpeg\ffmpeg.exe` as a **separate program** (communicating via pipes).
The binary is the unmodified "win64-gpl" build by BtbN (https://github.com/BtbN/FFmpeg-Builds),
which includes, among others, x264 (GPL v2+), libopus (BSD) and libvpx (BSD).
The license text is shipped as `resources\ffmpeg\LICENSE-ffmpeg.txt`.

**Source code offer:** the complete corresponding source code is available at
https://github.com/BtbN/FFmpeg-Builds (build scripts and pinned versions) and https://ffmpeg.org/download.html.
On request, we will provide a copy of the corresponding source code for at least three years
after we last distribute this version (contact: see EULA).

FFmpeg is a trademark of Fabrice Bellard, originator of the FFmpeg project.

## FabStream helper programs (mingw-w64 runtime, LLVM libc++ / compiler-rt)
`resources\native\fabstream-audio.exe` (sound capture) and `resources\native\fabstream-capture.exe` (GPU screen and
window capture) are FabStream's own programs, built with llvm-mingw (https://github.com/mstorsjo/llvm-mingw). They are
statically linked with the mingw-w64 runtime (Copyright (c) 2009, 2010 by the mingw-w64 project; Zope Public License
2.1 and public domain parts, https://www.mingw-w64.org) and with LLVM libc++, libunwind and compiler-rt (Apache License
2.0 with LLVM Exceptions, https://llvm.org/LICENSE.txt).

## H.264 / AAC patent notice
H.264 encoding may be subject to patent licenses (e.g. Via LA) in some countries.
Hardware encoders (NVENC/QSV/AMF) use the GPU vendor's driver-provided licenses.

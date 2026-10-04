# Security

## Reporting a vulnerability

Please report security problems privately to **f.grande@bluewin.ch** (subject "FabStream security") instead of opening a public issue. You will get an answer within a few days. Please include the FabStream version (Settings → Diagnostics) and steps to reproduce.

## How FabStream protects you

- **Stream keys** are stored encrypted with Windows DPAPI on your PC, never in settings files, never sent to Fabcom. Logs mask them.
- **No telemetry, no tracking.** FabStream only contacts GitHub (update notice) and – with a Premium subscription – the FabStream license server.
- **Sandboxed interface:** the app UI runs with Electron's context isolation and sandbox; it only talks to the main process through a fixed list of checked commands.
- **Verified updates only.** FabStream checks this repository for a new version on every start. An update is installed only after you click "Update & restart" **and** after FabStream has verified the Ed25519 signature of `SHA256SUMS.txt` with the key built into the app, checked that the signed list belongs to the new version, and compared the SHA-256 of the downloaded installer. A file that fails any check is deleted and never started.

## Verifying a download

Each release contains `SHA256SUMS.txt` (the SHA-256 of every file) and `SHA256SUMS.txt.sig`, an **Ed25519 signature** of that file made with the Fabcom release key. The same SHA-256 values are listed in the release notes.

1. Check the file hash (PowerShell):
   ```powershell
   Get-FileHash .\FabStream-Setup.exe -Algorithm SHA256
   ```
   Compare it with `SHA256SUMS.txt` / the release notes.
2. Optionally check the signature with OpenSSL 3:
   ```
   openssl pkeyutl -verify -pubin -inkey fabcom-release.pub -rawin -in SHA256SUMS.txt -sigfile SHA256SUMS.txt.sig
   ```
   with this public key saved as `fabcom-release.pub`:

```
-----BEGIN PUBLIC KEY-----
MCowBQYDK2VwAyEAh8Nf8oNHiAr0Yqkx5B/BQ71s6IolqmQlVymplmdpTdU=
-----END PUBLIC KEY-----
```

The in-app updater uses exactly this check: it never installs a file just because it was downloaded from a certain URL.

## Code signing

The installer is not code-signed yet (code-signing certificates for individual developers outside the US/Canada are not available at no cost). The **Microsoft Store version** of FabStream is signed by Microsoft and is not blocked by SmartScreen or Smart App Control.

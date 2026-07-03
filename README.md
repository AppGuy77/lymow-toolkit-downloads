# Lymow Toolkit — Downloads

Free installers for the **Lymow Toolkit**, a local companion dashboard for the
**Lymow One** robotic mower. It adds scheduling, a mow-history calendar, a
per-zone freshness map, RTK/link diagnostics + heat maps, and safety auto-pause
guards — features the official app doesn't offer.

> **Independent community project — not affiliated with, endorsed by, or
> supported by Lymow.** Use at your own risk.

## ⬇️ Download

- **[Download the latest release](https://github.com/AppGuy77/lymow-toolkit-downloads/releases/latest)**
- **Source code:** <https://github.com/AppGuy77/lymow-toolkit>

Grab the latest installer from the **[Releases page](../../releases/latest)**:

| Platform | File | Notes |
|---|---|---|
| **Windows** (recommended) | `LymowToolkitSetup-vX.Y.Z.msi` | Standard installer. Windows Defender leaves it alone. |
| Windows (alternative) | `LymowToolkitSetup-vX.Y.Z.exe` | Unsigned — may trigger a Windows Defender virus warning **because it's an unsigned file**. The `.msi` avoids that. |
| **macOS** | `lymow-mac-vX.Y.Z.tar.gz` | |
| **Linux / Ubuntu** | `lymow-ubuntu-vX.Y.Z.tar.gz` | |
| **Docker** | `lymow-docker-vX.Y.Z.tar.gz` | |

**Updating from an older `.exe` build?** Uninstall the old `.exe` first, then
install the `.msi` — or use the new `.exe` (same unsigned-file warning as above).

## ⚠️ Please read — safety

This software controls a **real machine with spinning blades**.

- **No warranty**, provided "as is." Not liable for injury, property damage, or a
  lost/damaged mower.
- **Supervise your mower.** Don't treat remote start/stop or the safety guards as
  a substitute for keeping people, pets, and hands clear of the blades.
- You sign in with **your own** Lymow account; nothing is shared with anyone else.

## Quick start

1. Install/unzip for your platform and launch it.
2. Open the printed address in a browser (e.g. `http://<your-computer-ip>:8787`),
   set a dashboard password, and sign in with your Lymow account.
3. **For scheduling:** keep the Toolkit running (install it as the always-on
   background service). Scheduled mows fire **from your computer**, so it must be
   running at the scheduled time — but the web page does **not** need to stay open.

> The **Calendar** and **Freshness** map read your *real* mow history from the
> Lymow cloud, so the first load takes a short moment, then it's cached.

## Found a bug or a security issue?

- **🐞 Bug or feature request:** open an [issue](../../issues/new/choose) — the
  form walks you through it. *(Please don't paste your account login or map/GPS
  data.)*
- **🔒 Security vulnerability:** report it **privately** via
  [Report a vulnerability](../../security/advisories/new) — never in a public
  issue. See our [Security Policy](SECURITY.md) for details.

## Acknowledgements

- **[d3dfantasy99/Lymow-HA](https://github.com/d3dfantasy99/Lymow-HA)** — the Home
  Assistant integration and authoritative device-protocol reference this project
  builds on. Big thanks.

## Community

👉 Facebook group: https://www.facebook.com/share/g/1Jc7YfPStf/

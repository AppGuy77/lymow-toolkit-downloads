## v1.45.0 — the mower really restarts after an error, and your own time zone


- 🔁 After an error the Toolkit now confirms the mower actually restarted, and keeps trying until it does
- ⏱️ "Wait before restart" is now honored by every fault, including a bumper jam
- 🎨 Coverage painting keeps itself up to date even with no browser open
- 🏠 "Mower returns to dock on an error" is now really sent to the mower, and stops disagreeing with auto-pause
- 🕐 Time zone has its own place in Settings, with daylight saving you can turn off
- 🐳 The Docker image is searchable now — pull it straight from Unraid, a UGREEN NAS or Docker Desktop


**Fixed**

- **The mower often did not restart after an error.** The Toolkit sent the resume and assumed it worked —
  on a raised cutting deck only one mower in four actually got going again. It now checks the mower is
  really moving and keeps trying until it is, then records whether it worked.
- **"Wait before restart (seconds)" was ignored for a bumper jam (E44)**, which cleared instantly. Every
  fault waits out the same countdown now.
- **Coverage painting fell behind when nobody was watching.** With the page closed the Toolkit stopped
  collecting the mowed path, so the map filled in wrong. It keeps up on its own now.
- **"Mower returns to dock on an error" was not sent.** Turning on Safety auto-pause said it had switched
  the setting off on the mower, but nothing reached the mower. The toggle also flipped itself back and
  claimed the mower had never reported it.
- **Timestamps ignored your time zone.** The mow calendar, the RTK logs and "last checked" used the zone of
  whichever browser you were looking at, so a late-evening mow could sit on the wrong day.
- **Automatic updates installed on the server's clock, not yours** — "install at 3:00 AM" meant something
  else entirely on a NAS set to UTC.
- **Docker and Home Assistant installs offered an automatic-update time** they cannot act on. Those update
  from the add-on page or with `docker compose pull`, and now say so.

**New**

- **Time zone is its own section in Settings.** It was buried in Night lights even though it sets every time
  the Toolkit shows and every time it acts on. It also shows the offset it is on right now.
- **Daylight saving can be turned off.** Leave it on and clocks move with the seasons as usual; turn it off
  and the Toolkit holds one offset from UTC all year.
- **The image is searchable on NAS systems.** Search "lymow" in Unraid's Apps tab, a UGREEN NAS or Docker
  Desktop and pull `appguy77/lymow-toolkit` — no more typing a full registry path.
- **The Lymow Toolkit name in the header opens the Facebook group.**

---

From **v1.43 or earlier**? v1.44 added update notifications and one-click updates, fixed the light coming on
at every mow, stopped the camera running unwatched on 4G, and fixed the Wi-Fi camera on macOS and Linux.
Full details:
[CHANGELOG](https://github.com/AppGuy77/lymow-toolkit-downloads/blob/main/CHANGELOG.md) ·
[Wiki](https://github.com/AppGuy77/lymow-toolkit-downloads/wiki)

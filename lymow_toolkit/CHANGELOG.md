## v1.44.2 — lifetime mow time, plus everything from v1.44.1

v1.44.1 was out less than a day, so it is all listed here too.


- ⏱️ Lifetime mow time was 60x too low — 120 hours showed as "2.0 h"
- 💡 The light no longer comes on at every mow, or stays on driving home
- 🌙 The night-light schedule no longer runs all day when From and To match
- 📷 The camera stops when you leave the page instead of burning 4G data
- ▶️ An unfinished mow says Resume, and goes back out once charged
- 🎛️ Blade speed, drive speed and cut height on the Remote fullscreen camera
- 💾 Start mow asks about unsaved cutting settings
- 🔔 The Overview only interrupts you for errors


**Fixed in v1.44.2**

- **Lifetime mow time was 60x too low** — 120 hours showed as "2.0 h". Fixes Home Assistant's total too.

**Fixed in v1.44.1**

- **The light came on at every mow**, and stayed on driving home. Mowers already stuck that way clear themselves.
- **The night-light schedule ran all day** when From and To matched.
- **The camera kept running after you left the page** — cellular data on 4G. It stops in seconds now.
- **An unfinished mow said "Start mow"**, which threw the rest of the cut away. It says **Resume**, with Cancel beside it. Pause only while docking.
- **A mow the mower took home on an error was dropped.** It goes back out once charged.
- **Start mow ignored unsaved cutting settings.** It asks which you meant.
- **Max drive speed showed the wrong number**, and moved in with the other mower settings.
- **The link heat map kept old colors** when you changed its thresholds.
- **The Overview interrupted you for everything.** Errors and recovery only — the rest goes to the log.

**New in v1.44.1**

- **Blade speed, drive speed and cut height on the Remote tab's fullscreen camera** — Off included. The Overview camera stays view-only.
- **Return to dock on an error** — the mower's own setting, now in the Toolkit so both apps agree.
- **The event log is kept on disk** — it survives restarts.

---

From **v1.43 or earlier**? v1.44.0 added update notifications and one-click updates, and fixed the
Wi-Fi camera on macOS and Linux. Full details:
[CHANGELOG](https://github.com/AppGuy77/lymow-toolkit-downloads/blob/main/CHANGELOG.md) ·
[Wiki](https://github.com/AppGuy77/lymow-toolkit-downloads/wiki)

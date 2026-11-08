Lymow Toolkit v2.14.9

Mower settings in step with the official Lymow app, mower clocks that follow daylight saving, the camera readings bar always on, the Singapore region and seven more languages. It keeps your sign-in, settings, maps, layout and history — just update.


- **Settings match the official app** — Pause on RTK loss, Return to dock on error, the light window and the time zone are one setting, kept by the mower.
- **Mower clocks** — each mower's clock kept right through daylight saving.
- **Readings bar** — always on, on every mower camera.
- **Singapore** — sign in from the new region.
- **Seven more languages** — Simplified Chinese, Polish, Croatian, Slovenian, Norwegian, Malay, Tamil.


## New

- **Mower settings now match the official Lymow app.** A setting both apps have is one setting, kept by the mower: change it in the Toolkit and the official app shows it; change it in the app and the Toolkit shows it. This covers **Pause on RTK loss**, **Return to dock on error**, the **light window** (Night Mode) and the mower's **time zone**. Pause on RTK loss is the official app's own switch, now in the Toolkit's RTK window (Map → RTK precision) with the Toolkit's precision limits under it. The Toolkit's own extras — sunset-to-sunrise lights, auto-resume, the daylight-saving offset on older firmware — keep working as you set them.
- **Mower clocks (Settings → Time zone).** Each mower keeps its own clock for its schedules, night lights and Recharge & Resume hours, and the Toolkit keeps it right through daylight saving. Mower firmware v2.1.51.2 and newer keeps a time zone by name and adjusts for daylight saving itself; older firmware gets the correct offset at each change. The list shows every mower's firmware and zone, with **Set now** to write the zone you picked. Schedules made in the official app show on the Calendar at the time the mower actually runs them after a daylight-saving change.
- **The readings bar is always on** — on the Remote camera, a mower's camera window and every grid tile, whether the camera is off, starting, live or fullscreen. Before any reading arrives it says "No readings yet".
- **Singapore region** at sign-in (Asia Pacific (Singapore)), including the away link.
- **Seven more languages:** Simplified Chinese, Polish, Croatian, Slovenian, Norwegian, Malay and Tamil. The Toolkit now ships in 24 languages (Settings → Language).

## Fixed

- **Changing the time zone should now redraw the logs, calendar and night lights at once** instead of after a reload.
- **On a phone the camera window takes the screen's width**, so the readings, Keep camera on and the task buttons never overlap.
- **RTK "Add a base" should no longer scroll the page sideways** in phone landscape, and the Home Assistant **Restore / Update file picker should fit a small phone**.
- **Error names as the official app names them:** 48 is "Bumper jammed (reverse timeout)", 81 and 82 are "RTK signal lost"; their help text matches.
- **Mower profile versions labeled correctly:** MCU, wheel motor and blade motor firmware (the row used to read "MCU / board").

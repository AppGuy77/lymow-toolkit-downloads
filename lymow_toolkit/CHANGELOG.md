Lymow Toolkit v2.8.0

An update for everyone on v2.7. It keeps your sign-in, settings, maps and history — just re-download and install.


- **The event log says who did what.** Every start, pause, resume, trip home and charge names who caused it — or says "not commanded by the Toolkit". Every line carries its date, start and end lines name the zones, 🟢 🟡 🟣 mark started, paused and resumed, and **⬇️ Download (.txt)** saves the whole log.
- **Log out of all devices.** The Log out button asks: this device, or all devices on your Lymow account.
- **Satellite imagery lines up per RTK base.** With two or more RTK bases: Settings → Multiple RTK → **Align imagery** on each base.
- **Auto-recover should no longer loop on the same obstacle**, and never restarts a mower that reports it is outside its map.
- **Security patches.**


## The event log

The event log now records every change in what the mower is doing — started, resumed, paused, heading home, docked, charging, fully charged, waiting, remote control, updating — and who caused it: the part of the Toolkit that sent the command (a button, the scheduler, auto-recover, the RTK guard, Recharge & Resume), or **not commanded by the Toolkit** when the official app, another Toolkit on the same account or the mower itself did it. A start the mower's own schedule made is named as such when the mower reports it.

Every line carries its date. Start, resume and end lines say which zones the task covers — "2 of 5 zones", "all 5 zones", or "zones not reported yet" followed by a line naming them once the mower does. Colored markers make the lines easy to find: 🟢 started, 🟡 paused, 🟣 resumed. RTK base changes are logged with the last 4 characters of each serial. **⬇️ Download (.txt)** beside Copy saves the whole recorded log, which is what to attach to a bug report.

**Record events** is switched on once for everyone with this update. Turned off, it now hides only the mower's error and warning codes; starts, stops, docking and the Toolkit's own commands are always recorded. Every event also has a plain-English name instead of an internal one.

## Log out of all devices

The **Log out** button now asks where to log out. **This device** signs this Toolkit out, as before. **All devices** ends every session on your Lymow account at once — the official Lymow app on every phone and tablet, every Toolkit and Home Assistant add-on — asks you to confirm, and then checks with Lymow that the old session is refused. Everyone signs in again with your password; if you think it leaked, change it in the official app first. A device that is already connected can keep working for up to an hour.

## Satellite imagery per RTK base

Each RTK base puts your maps on the satellite photo a little differently, so with two or more bases one alignment per yard is off for every base but one. In **Settings → Multiple RTK** each base now shows whether it is aligned for the imagery provider on screen and has an **Align imagery** button: it backs up the mower's current map, loads one of that base's maps (with the mower on its dock), and opens the map unlocked so you drag the photo into place and lock it. Then it offers the next base, or putting your usual map back. Switching bases should switch the alignment by itself, in Fleet Mode too. Your existing alignment is kept for the base the mower is on and stays in use for any base you have not aligned. A yard with one base is unchanged.

## RTK base only switched on the dock

Restoring a map made on another RTK base — or a multi-map run switching to one — now switches the base only with the mower on its dock. A restore away from the dock is refused with a message, and a multi-map run sends the mower home first.

## Auto-recover

Auto-recover should no longer restart the mower again and again into the same obstacle: the same fault coming back within 10 minutes of a restart counts as one incident, and the retry count resets only after 30 seconds of mowing. A mower that reports it is outside its map, or that its route planner lost its position, is never restarted. A fault code the Toolkit does not recognize is left alone unless you switch on its row — **A code the Toolkit doesn't recognize** — in Warnings & errors.

## Other fixes

- Safety settings changed in Fleet Mode for a mower other than the dashboard one should no longer revert after a restart, and Copy settings to other mowers applies at once to a mower that is connected.
- When the mower reports no Recharge & Resume hours, the Toolkit no longer sends it back out after a charge, and Recharge & Resume says so.
- The fault list's group names and descriptions (Settings → Warnings & errors) show in your language instead of English, and every translation uses one wording per button and addresses you the same way throughout.

## Security patches

This release includes security patches. Updating is recommended for everyone.

Lymow Toolkit v2.8.1

An update for everyone on v2.8.0. It keeps your sign-in, settings, maps and history — just update.


- **Far less cloud traffic.** When the mower is stopped with nothing to capture, the Toolkit disconnects from the Lymow cloud like the official app does when it is closed, and connects again the moment the mower starts, you open the page or a schedule is due.
- **Lymow's own notifications arrive through the Toolkit** — mowing started, rain, charging faults — one notification per event.
- **Cancel mows the Toolkit didn't start** (Settings → Warnings & errors, off by default). Schedules made in the official app are never canceled.
- **Warnings & errors can be the same for all mowers**, or set per mower from a list.
- **"Job complete" only when the mower says so** — a canceled job says "Job canceled".


## Far less cloud traffic

When the mower is stopped with nothing to capture — parked, charging, paused, or halted on an error — the Toolkit now disconnects from the Lymow cloud a minute later, the way the official app does when it is closed. It connects again by itself the moment Lymow says the mower started, resumed or stopped on an error, when you open the page, when anything is sent to the mower (Home Assistant included), for the camera, and 10 minutes before a Toolkit schedule. Everything it does — auto-resume, the guards, auto-cancel — starts at once when it wakes.

Out mowing, the mower reports its position and status by itself, so the Toolkit only sends one message every 30 seconds. With a heat map on it takes every RTK reading the mower's board makes, so the map has no gaps; with only a guard on, one every 15 seconds. With the page open everything is live every 3 seconds. The mowed-area painting catches up once when the mower stops and once when you open the page.

It stays connected while something needs it: a guard holding its pause, a recovery waiting to resume, the mow queue or a multi-map run, a light command not yet confirmed, or — with the **Fully charged** notification on — the battery, read every 5 minutes on the charger until it gets there. A mower that does not answer at all (switched off, no signal) is asked once a minute, and after 5 minutes left alone unless you are looking at it.

**Stay connected all the time** (Settings → Remote & connectivity) keeps the old behavior. Advanced Data → **Cloud traffic** shows the mode and how many messages were sent in the last hour.

## Lymow's own notifications

The messages the official Lymow app gets — mowing started, rain, charging faults and the rest — now arrive through the Toolkit's notifications, on whichever route you use: browser push or the Home Assistant Companion app. Each event is one notification, titled with the mower's name, in Lymow's words. There is no separate switch: notifications are on or off, as before.

For this, the Toolkit keeps your mower's Lymow notification level on **All** — the same setting as in the official app, so both always show the same value. What reaches your phone is still chosen in the Toolkit's own notification list.

## Cancel mows the Toolkit didn't start

Settings → Warnings & errors → **Cancel mows the Toolkit didn't start** (off by default). When it is on, a new mow started by hand from the official app, with the mower's own button, or by another Toolkit on the account is ended within seconds, and **After canceling** decides what the mower does: go to the dock, or stay where it stopped. It is never canceled when this Toolkit started it, when the mower carries on after a charge, or when a schedule made in the official app started it — the Toolkit reads those schedules from the mower and checks them before it cancels anything. The event log and your notifications say what happened.

## Warnings & errors for all mowers, or per mower

With more than one mower, **Same settings for all mowers** at the top of Warnings & errors gives every mower one set of settings — fault handling, auto-resume, canceling mows the Toolkit didn't start, the RTK and link guards, the heat maps and logs — a mower added later included. Turned off, the mowers show as a list: tap the ones you are changing, and Save applies what is shown to each of them. Every save says which mowers it was for, and each mower's event log records it.

## Notifications that say how a job ended

**Job complete** is sent only when the mower itself reports that the job completed. A canceled job is **Job canceled**, and a job that ended without a report is **Job ended**. A trip home after a cancel or for rain is plain **Docking**; **Docking to recharge** only when the mower is at its own return battery level.

## The event log

The event log should now tell the truth about who did what. Every change in what the mower is doing is recorded as it happens, not only the ones a regular check caught. Driving the mower from the Remote tab, and changing the deck or blades there, is credited to the Toolkit. Every command the Toolkit sends is listed as **📤 Sent to the mower**. A mow started by the mower's own schedule is named as such every time, and a mow the mower announces a moment after it started is named in a follow-up line.

## Other fixes

- A multi-map run should always put your map back on its own RTK base when it finishes, a canceled run should go home, and a failed restore never deletes the only copy of your map.
- After you cancel, pause or dock the mower, the RTK and link guards no longer resume it later.
- Auto-recover should never send a mower back out from its dock.
- Phone notifications should keep working: a phone renews its subscription by itself, and every browser can receive notifications (the "Allow desktop browsers" switch is gone).
- Home Assistant "Mowing started" and "Resuming job" notifications offer **Stop and dock**.
- The Home Assistant add-on's setup should give the right instruction when the Mosquitto broker is not running.
- Accounts in the Hong Kong region should be able to add a mower again.
- The official app's schedules on the Calendar show when they were last read from the mower.

## Updates

Automatic updates are switched on once for every install, at 3:00 AM when every mower is idle — you can turn them off in the Updates tab. An update now waits until every mower is idle, not only the one on screen. On Linux and macOS an update installs the new version's packages first. macOS should update without starting a second copy. Docker installs get step-by-step instructions for automatic updates in the Updates tab, and the Home Assistant add-on switches on Home Assistant's own Auto update and Watchdog.

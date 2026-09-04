Lymow Toolkit v1.55.0

Everything below is a change from v1.54.2.


- Push notifications on your phone through Home Assistant: mowing started, each zone finished, mow completed, returning to dock, docked, fully charged, safety guards pausing and recovering, and the mower's own messages — through your Setup token or automatically as the HA add-on. Choose groups and phones under Settings → Home Assistant → Push notifications.
- The camera reconnects by itself after a lost or frozen picture in every link mode, retrying every 5 s (WiFi only as soon as the signal is at least -70 dBm), on both the Remote and Overview cameras.
- The Camera link choice (Auto / WiFi / 4G) is saved on the server, so it follows you to every browser and phone.
- No picture, no driving: remote-control driving now requires a live camera picture, enforced on the server like the blades; a frozen picture disables the joystick within seconds.
- Multi-zone cross-cut mows no longer paint the next zone's first pass in both colors; yards with 30+ zones keep every zone's paint.
- "Pause on Float" now works: the toolkit read the mower's fix-quality numbers wrong (a real RTK Float showed as "RTK fixed"). Fixed from the reference everywhere — guard, heat map, Home Assistant sensor, dashboard.
- Every safety system stands on its own switch (auto-pause, auto-clear & resume, RTK guards): turning one off no longer disables the others; dependent settings are greyed on the same screen and cannot be switched on without their parent.
- Auto-clear faults and resume, simplified: one switch, one Attempts count, and every fault restarts unless you exclude it in the fault list — which now shows every code the mower can report.


## Push notifications through Home Assistant

With Home Assistant enabled, the Toolkit now sends the mower's events to every phone signed in to the
Home Assistant companion app: **mowing started**, **each zone finished** (with the zone's name and
"n of m"), **mow completed** (zones and area), **returning to dock**, **docked and charging**, **fully
charged**, the safety guards **pausing and recovering**, **faults**, and the mower's own messages
(rain detected, charging abnormal, geo-fence, new firmware).

It reaches Home Assistant through the access token you pasted for **Setup Home Assistant**, or
automatically when the Toolkit runs as the **Home Assistant add-on** — nothing to paste there. Under
**Settings → Home Assistant → Push notifications** you choose which event groups to receive (mowing
progress, each zone finished, docking and charging, problems and safety guards, messages from the
mower) and which phones (nothing ticked = every phone). **Send test notification** tells you what Home
Assistant actually did. Each group replaces its previous notification on the phone instead of
stacking, so a 30-zone yard shows one updating "Finished zone…" line rather than thirty.

Every event is also published to Home Assistant as an **Events** entity on the mower's device, for
your own automations, blueprints and speaker announcements — that part needs no token at all.
The notification text follows the Toolkit's language setting.

## The camera reconnects after a lost picture, and nothing drives blind

Before, only **Auto** healed a lost picture. **WiFi only** now retries every 5 seconds as soon as the
mower's own WiFi signal is at least -70 dBm (reachability from the toolkit machine is only used when
the mower reports no signal), showing the live reading while it waits. **4G only** retries every 5
seconds. A **frozen** picture counts as lost: no decoded frame for 6 seconds disables the joystick,
stops the blades, leaves remote control and starts the reconnect. Both the **Remote** camera and the
**Overview** camera do this, for as long as the camera is open.

**No picture, no driving.** The server now refuses a drive command unless a live picture is arriving,
exactly as it has refused to spin the blades since v1.38.2. A stop command is always accepted.

## Cross-cut colors on multi-zone mows

Mowing two or more zones with **Add a cross-cut pass** painted the second zone's first pass in both
colors at once (green fill under an orange trail). Each zone's crossing pass now ends when the zone
does, and the paint archive holds up to 128 zones so yards with 30+ cross-cut zones keep every zone's
paint through the whole mow.

## "Pause on Float" now works — the fix-quality numbers were wrong

The RTK guard's **Also pause on Float fix** never fired because the toolkit had the mower's
fix-quality enum wrong since the guard shipped: it treated 1 as Float and 2 as RTK fixed. The
mower's app (and the Lymow-HA reference) use **0 = no signal, 1 = single point (plain GPS), 2 = RTK
Float, 3 = RTK Fixed**. A real Float fix therefore arrived as 2, was labeled "RTK fixed" in green on
every screen, and the guard's Float rule never matched. This is corrected from the reference in the
guard, the heat map's Float/No-fix overlay, the RTK-fault "wait for the fix" check, the Home
Assistant RTK sensor and the dashboard pill, and audit gate 5 now checks the enum against the
reference so it cannot drift again. **After updating, a Float fix shows as Float, in orange.** If
your Home Assistant automations compared the raw `position_quality` number, 3 is now "fixed".

## Every safety system on its own switch

Three independent systems, each with its own master, none depending on another:

- **Safety auto-pause** (Settings → Warnings & errors): stop the mower when a fault or resistance
  appears while it is driving. Its master governs only those two rules.
- **Auto-clear faults and resume** (same panel): clear the error, wait, resume, confirm, repeat up to
  **Attempts** times. It was called "Auto-resume after a stop" and was silently disabled whenever
  Safety auto-pause was off. It is not any more.
- **RTK precision guard and RTK link guard** (Map tab): each needed the Settings master as well as
  its own switch, on two different screens. Now only its own.

A setting that depends on another switch is **greyed out until that switch is on, on the same
screen**, and the toolkit **refuses** to switch it on otherwise ("'Also pause on Float fix' needs
'Pause the mow when precision degrades' switched on first"). A setting saved before this version
that is on under an off parent shows a **not active — needs …** badge instead of pretending to work.
**Cancel task** no longer disarms recovery for a mow later started from the official app or the
mower's own schedule.

## Auto-clear faults and resume, simplified

One switch, one **Attempts** count (1 to 100, no "forever"), one **Wait before restart**. **Every
fault the mower can report is restarted unless you exclude it** in the fault list, which now lists
all 114 codes (49 were not listed before, and only 15 restarted by default). A row can carry its own
attempt count instead of the global one. RTK and positioning faults are rows of the same list under
**RTK & positioning** (their wait-for-the-fix recovery is unchanged); the separate switch on the Map
tab is gone. The nine safety-critical faults are listed under **Safety-critical**, locked: the
toolkit never clears, restarts or even pauses the mower while one is active. On upgrade every code
becomes included, your per-code counts survive as overrides, and "stopped with no fault code" stays
excluded.

## The RTK guard reports what it did

A PAUSE the mower ignores is logged as `rtk_pause_unconfirmed` with the mower's status after the
third send. A Float or No-fix inside the dock grace radius is logged as `rtk_guard_blocked` with the
reason. While either guard is armed and the mower is working, it is watched every 5 seconds instead
of 10, so a short episode cannot fall between two polls.

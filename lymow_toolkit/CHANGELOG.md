Lymow Toolkit v2.9.3

An update for everyone on v2.9.1 or v2.9.2. It keeps your sign-in, settings, maps, layout and history — just update.


- **The camera picture through the Toolkit should stay clean in motion** (the away link, Home Assistant), and it reopens at once.
- **Schedules follow your charge rules** (Recharge & Resume level, 80% when off, and its hours), and **zones mow in the order you pick**.
- **Phones:** the header and tabs are in a **☰** menu; the fullscreen map should fill the screen.
- **Keep for (days)** on every log, and the status bar's items picked on the bar itself.


## Camera

- **The picture through the Toolkit should stay clean in motion.** On the away link and in Home Assistant it smeared
  into blocks whenever the mower moved.
- **It reopens at once.** After you leave the Remote or close a camera view, the WiFi picture stays ready for 5 minutes
  on your home network; **Stop camera** ends it right away. Opening the Remote tab gets it ready.
- **Camera failures say what happened in plain words**, for example that the mower did not answer on WiFi.

## Scheduling

- **A scheduled mow waits for charge.** It starts once the battery reaches the Recharge & Resume resume level, or 80%
  when Recharge & Resume is off. With Recharge & Resume on, it starts only between its Start Time and End Time.
- **Skipped, not lost silently.** When the hours or the day run out first, the mow is skipped and the event log and your
  phone say why. A start the mower doesn't act on is tried again.
- **Mow order:** Pick zones… lists the zones in the order you tick them; drag one to move it. That is the order the
  mower is sent them in.
- **Official-app schedules** run on the mower itself, so the Toolkit's rules don't apply to them, and the Calendar says
  so. **✎ Edit in the Toolkit** makes one a Toolkit schedule: when you save, the Toolkit removes it from the Lymow app and
  checks with the mower that it did, so it never runs twice. Each zone mows with its own saved cut settings.

## Phones

- The header and the tabs are in the **☰** menu in the upper-right corner, upright or sideways. The page starts at the
  top.
- **The fullscreen map should fill the screen** on every phone (a saved map height cut it short), with the map toggles
  below the status bar. Map settings open or closed is the same on every phone.

## The status bar

- With **🔒 Layout** unlocked, the status bar shows every item as a chip: tap one to show (✓) or hide (+) it. The
  Overview's map and the Remote's camera views each keep their own choice, and a phone and a computer each keep theirs.
- **Position** and **Last finished mow** can be added.

## Remote control

- **Joystick moves made while the mower was out of reach should no longer run when it reconnects.** A move is not sent
  to a mower that has stopped answering, and driving needs a camera picture from the last 1.5 seconds. A stop always
  goes through.
- **Arrow responsiveness** (Remote → Camera options): the arrow keys push the joystick a third of the way (1 Light),
  half (2 Middle) or all the way (3 Full). The first arrow press after each camera start asks which (click, or press 1, 2 or 3), and the same keys change it while you drive.

## Logs

- **Keep for (days)** beside every log you can switch on: the Event log, Telemetry history, Battery & charging and the
  RTK log (Advanced Data), and the Link heat and Precision heat maps (Map ⚙️). Each keeps its last 1–365 days, 30 unless
  you change it; older entries are removed every hour.

## Also

- On a computer, the tabs should stay in view below the header when you scroll.
- **macOS:** a fresh install from the Downloads folder should keep the camera's files; the installer's move to `/usr/local/lymow-toolkit` left them behind.

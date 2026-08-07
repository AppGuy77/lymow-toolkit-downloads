## v1.46.0 — every fault has its own restart setting


- 🩹 Every error and warning now has its own switch and its own number of restart attempts, grouped by the part of the mower
- 🔌 Faults that were never meant to be retried now stop and wait for you — a docked mower no longer clears Charging Not Detected and drives off every few minutes
- 🔋 New battery and charging log, with any fault the mower reported at the time
- 🛰 New Float and No-fix colors on the precision map — spots with no satellite fix were never recorded before
- 🗺️ Road names on the satellite map with Satellite and Street map both on
- 💾 Settings stopped overwriting each other — map toggles and the satellite alignment no longer come back reset after an update
- 📱 Help bubbles are tappable and readable on a phone


**New**

- **Every fault has its own restart setting.** Under Settings → Warnings & errors, the errors and
  warnings the mower can report are grouped by the part of the machine they come from — blade and
  cutting, drive and wheels, stuck/slipping/obstacles, docking/charging/battery, navigation and path,
  sensors and camera, internal. Open a category to see what each fault means and choose whether the
  toolkit restarts the mow for it, and how many times. Previously one switch and one "max restart
  tries" box covered every fault at once.
- **A battery and charging log.** Advanced Data → Battery & charging records every time the mower
  connected to or left the charger: how much charge it gained, how long that took, and how fast it
  drains while parked. Any fault the mower reported at that moment is shown on the row. It opens with
  a plain-English summary of the last day.
- **Float and No-fix areas on the precision heat map.** Two more colors, switched on together beside
  the existing three, showing where the mower only managed a rough fix and where it had no satellite
  fix at all. They paint over the precision colors and can be shown with the precision heat off.
- **Road names on the satellite map.** With Satellite and Street map both on, roads and place names
  are drawn over the aerial photo.

**Fixed**

- **Unrecognised faults were cleared and restarted forever.** Any fault the toolkit did not have a rule
  for was cleared and the mow restarted every 15 seconds, with no limit. The clearest case was
  Charging Not Detected (#51): a mower sitting on the dock would clear the error, drive off, return,
  and repeat every few minutes through the night. Those faults now stop and alert you. Jams, snags and
  slips still restart automatically.
- **Lifted, tilted, unsafe drop and out of bounds are now left completely alone.** While one of these
  is active the toolkit sends the mower nothing — it does not clear the error and does not restart it.
- **Motor Overheat and Blade Over-Temperature were retried like any other fault.** They now wait for
  you unless you switch them on.
- **Saving one setting could discard another.** Settings saved seconds apart could overwrite each
  other, which is why map toggles, the satellite image alignment and occasionally a guard setting came
  back reset after an update. Each setting is now written on its own and completed in full, so an
  interrupted save can no longer damage the file either.
- **The Satellite and Street map switches did not remember themselves** in the browser, so they relied
  entirely on the copy held by the toolkit.
- **Help was hard to use on a phone.** The ? bubbles were about a third of the size a finger needs, and
  roughly a third of all help in the app could only be seen by hovering a mouse — unreachable on a
  touch screen. Hold any control to read its help. Help opening near the bottom of the screen was cut
  off and now flips above.
- **The glossary's Overview / Remote / Calendar / Advanced Data / Settings buttons did nothing.**
- **Settings windows were much narrower than intended**, which made them needlessly long, and the rows
  did not line up.

**Changed**

- Blade-warning monitoring, the bumper-jam (E44) auto-clear and its try count, the shared restart cap,
  and the low-battery return to dock no longer have their own boxes — each is now the setting on its
  own fault's row. Existing choices carry over.
- "Street map" now means roads everywhere: on its own with satellite off, and as labels over the photo
  with satellite on.

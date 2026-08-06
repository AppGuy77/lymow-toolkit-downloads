## v1.45.2 — multi-pass really uses each pass's settings


- 🔁 Multi-pass now uses each pass's own spacing, height and angle — every pass after the first used to run on the first one's
- 🏠 No more driving home and back between passes
- ✂️ Power and Turbo can now be picked for a scheduled mow
- 🗺️ Mowing across maps no longer sends an already-docked mower to the dock, and waits for the new map to load before it mows
- 🎨 The mowed paint is drawn at the mower's real 16-inch cut width


**Fixed**

- **Multi-pass ignored the settings you gave each pass.** Set 35 cm, then 30, then 25 and every pass cut
  at 35. The same went for a different height or angle per pass. The mower only accepts a change to its
  saved settings while it is idle, and between passes it sits paused — where it stays until something
  ends the finished pass. So the change was refused every time and the pass mowed on with the previous
  one's settings. Each pass now gets its own settings, confirmed on the mower before it starts cutting.
- **A pass that cannot be set up no longer mows anyway.** It used to carry on at the previous pass's
  settings, which you could only discover by looking at the lawn. The run now stops and tells you which
  setting could not be applied.
- **Multi-pass drove all the way home and back between passes.** When a pass finished, the mower returned
  to the dock, charged for a moment and drove back out to carry on — cutting nothing the whole time. It
  now picks up the next pass from where it stands. A genuine low-battery return to charge is never
  interrupted.
- **Power and Turbo could not be chosen for a scheduled mow.** The blade speed list in Scheduled mows was
  left on an older numbering, so picking Power scheduled Eco and picking Turbo scheduled Standard. Please
  check the blade speed on any schedule you already have — the old choice cannot be told apart from a
  correct one, so those schedules read as Eco or Standard until you set them again.
- **A blade speed of Power or Turbo was named wrongly** in the confirmation that appears before saving
  cutting settings — the one screen whose job is to tell you what you are about to change.
- **Mowing across maps began by sending the mower to the dock**, even when it was already sitting on it.
  It now only goes home when it is actually out working. It still returns to the dock before switching
  from one map to the next, because that is how it gets to the other map.
- **Mowing across maps could sit on "restoring" and then mow nothing.** The Toolkit was not asking the
  mower for its map, so it could not tell the new map had loaded, and after a wait it started the mow
  anyway against the old map — where the zones did not exist, so the mower did not move. It now confirms
  the mower is really running the restored map, shows what it is waiting for, and refuses to mow a map it
  could not confirm.
- **Zones you picked stayed picked after the map changed.** Restoring a saved map left your old selection
  in place, still labelled as belonging to the map you restored — so pressing Mow tried to load that map
  again. Changing the map now clears the selection, and both maps stay on screen: the active one solid,
  the one you left dotted.
- **The mowed paint was far too wide** — about 1.7 m, four times the mower's 16-inch cut. It is now drawn
  at true width, so missed strips and overlap show up honestly.

---

Coming from **v1.44 or earlier**? v1.45 made the map paint what the mower actually cut, made the mower
really restart after an error, and gave time zone its own section in Settings. Full details:
[CHANGELOG](https://github.com/AppGuy77/lymow-toolkit-downloads/blob/main/CHANGELOG.md) ·
[Wiki](https://github.com/AppGuy77/lymow-toolkit-downloads/wiki)

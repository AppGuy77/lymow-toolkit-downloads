## v1.45.1 — hotfix: the map paints what the mower actually cut


- 🎨 The map now fills in as the mower cuts — it used to show almost nothing at 60% done
- ⚡ A charging bolt on the battery, visible in every mode including remote control
- 📊 Remote control no longer hides the status — you can see Charging, or a mow on hold, while you drive
- ▶️ Resume now appears for a mow you paused in the Lymow app, instead of "Start mow"
- 📍 Zones and paint sit more accurately on the satellite image


**Fixed**

- **The mowed area barely showed on the map.** A mow at 60% done could leave the map looking untouched,
  with only the narrow strips filled in. The Toolkit was drawing the mower's report as a thin trail of
  points instead of the areas it actually describes, so nearly all of the cut was invisible. The map now
  fills in the mowed ground the way the Lymow app does, including the unmowed patches left inside a zone,
  and it keeps up while the mow is still running rather than only catching up at the end.
- **Zones the mower had finished did not fill in.** Completed zones now fill as soon as the mower says it
  has finished them, instead of waiting for the whole mow to end.
- **The status disappeared while using remote control.** The mower can only report one status at a time,
  so "Remote control" replaced everything else — you could not see that it was charging, or that a mow was
  waiting on hold. It now shows what the mower is really doing while you drive it.
- **There was no way to tell if the mower was charging** unless it happened to be reporting "Charging".
  A charging bolt now sits next to the battery wherever the battery is shown, and it stays correct in
  remote control, on the way to the dock, and mid-mow.
- **"Start mow" appeared instead of "Resume"** for a mow started or paused in the Lymow app, or one that
  was already running when the Toolkit was opened or restarted. Pressing it began a brand-new mow and threw
  away the rest of the cut. The Toolkit now recognizes an unfinished mow it did not personally watch begin,
  and offers Resume — the same as the Lymow app.
- **Buttons could act on a stale status.** Some updates from the mower left the Toolkit's controls working
  from a reading it had already moved on from.
- **The map sat slightly askew on the satellite image.** Zones, paint and the heat maps drifted further from
  their true position the further they were from the mower's base station — roughly half a metre per 200
  metres. Everything is placed accurately now, so expect your zones to shift very slightly and line up
  better with what you see underneath.

---

Coming from **v1.44 or earlier**? v1.45 made the mower really restart after an error, gave time zone its own
section in Settings, and made the Docker image searchable on NAS systems. Full details:
[CHANGELOG](https://github.com/AppGuy77/lymow-toolkit-downloads/blob/main/CHANGELOG.md) ·
[Wiki](https://github.com/AppGuy77/lymow-toolkit-downloads/wiki)

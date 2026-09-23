Lymow Toolkit v2.7.2

An update for everyone on v2.7.0 or v2.7.1. It keeps your sign-in, settings, maps and history — just re-download and install.


- **Restoring a map is safe again.** A restore no longer changes the mower's RTK base — the v2.7.1 auto-bind could corrupt the map (it stopped showing in the official app and the mower refused zone edits with "cannot find objects"). Restore now touches the map only.
- **Indicator LEDs.** Settings → Lights can turn the mower's red and green body LEDs — the official app's "Vehicle LED" — on or off, and switch them on during your night-light hours while it mows. It shows what the mower itself reports.
- **Bind an RTK base on its own.** Multiple RTK now has a Bind button — the way to switch bases now that restore leaves the base alone: bind the correct base first, then restore.


## Restoring a map no longer touches the RTK base

v2.7.1 tried to bind the map's RTK base as part of restoring it. On some mowers that re-initialization corrupted the map: it stopped rendering in the official app and the mower rejected zone changes with "cannot find objects." A restore now writes only the map — it leaves whatever base the mower is on alone — so this can't happen. If you restored a map on v2.7.1 and it broke, restore it again on v2.7.2 and it comes back clean.

## Indicator LEDs

The Settings → Night lights section is now just **Lights**, and it can control the mower's red and green body status LEDs — what the official Lymow app calls "Vehicle LED." Turn them on or off, and tick **Include indicator LEDs** to have them come on during your night-light hours while the mower is working. The toggle always shows the state the mower itself reports, and a change here shows in the official app too.

## Multiple RTK — bind is its own step

Because a restore no longer changes the base, switching bases is now a deliberate action: **Multiple RTK → Bind** binds the mower to a base (it re-initializes the mower to re-localize on it). If a saved map belongs to a different base, bind that base first, then restore the map. Single-base yards never need this.

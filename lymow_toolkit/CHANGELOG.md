Lymow Toolkit v2.7.3

An update for everyone on v2.7.0 or v2.7.1. It keeps your sign-in, settings, maps and history — just re-download and install.


- **Restoring a map with more than one RTK base now works right.** When you restore a saved map — or a multi-map run switches to one — the Toolkit binds that map's RTK base **first**, then loads the map, so it lands in the right place instead of offset (or corrupted, which an earlier build could do). It is automatic: in Settings → Multiple RTK you only say which base a map belongs to. A map you leave unset is restored on whatever base the mower is on now.
- **Indicator LEDs.** Settings → **Lights** (renamed from Night lights) can turn the mower's red and green body LEDs — the official app's "Vehicle LED" — on or off, and switch them on during your night-light hours while it mows. It shows what the mower itself reports.


## Restoring a map binds the right RTK base first — by itself

If you run more than one RTK base station, every saved map was surveyed on one particular base. Restoring a map onto the wrong base makes the mower mow offset by the distance between the bases. Now the Toolkit binds the map's base **before** it loads the map — re-initializing the mower so it re-localizes on the correct base first — on a manual restore and at every switch of a multi-map run. You never bind by hand: in **Settings → Multiple RTK** you just assign each saved map to the base it belongs to (maps you back up from the Toolkit are assigned for you). A map with no base assigned is restored on the base the mower is already on. A single-base yard needs none of this and is unchanged.

## Indicator LEDs

The Settings → Night lights section is now **Lights**, and it can control the mower's red and green body status LEDs — what the official Lymow app calls "Vehicle LED." Turn them on or off, and tick **Include indicator LEDs** to have them come on during your night-light hours while the mower is working. The toggle always shows the state the mower itself reports, and a change here shows in the official app too. In Fleet Mode, pick the mower from the Lights selector.

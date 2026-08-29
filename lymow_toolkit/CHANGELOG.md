Lymow Toolkit v1.51.7

Everything below is a change from v1.51.6.


- Zones with their own stripe angle should now all mow at that angle: several custom zones saved or mowed together kept only the last zone's settings — the rest fell back to the global.
- Saving global settings now asks whether custom zones keep their settings or are overridden; Override deletes them on the mower and shows what the mower kept.
- The Toolkit and the official app now share one set of settings — a global saved in either shows up in the other.
- Resume should now be offered after a mid-mow power cycle (battery swap), the way the official app does.


## Custom zone angles that actually held

Field report (2026-08-28): global angle 36°, three zones set to their own angle (two fixed, one
Optimized), all mowed in one run — one zone mowed its angle, the other two mowed the global with
"a million turns". Cause: the Toolkit wrote the zones' settings to the mower one zone at a time,
and each write also carried the other zones as the Toolkit last saw them, so every write undid the
one before it. Only the last zone written kept its settings. All zones now go to the mower in a
single write, and the event log records what each zone was given.

## Keep custom or override

Saving global settings while some zones have custom settings now asks what to do — the same choice
the official app offers. **Keep custom:** each zone keeps only the values it customized; every other
setting on every zone follows the new global. **Override zones:** the zones' custom settings are
deleted on the mower so all zones use the global, and a result box shows what the mower actually
kept (cleared zones, or any zone that kept settings). Previously the Toolkit had no choice here,
and its override copied the global onto every zone, which made every setting look custom.

The saving rule itself has not changed and is now stated in the panel: nothing selected = global
for all zones; zones selected = only the values that differ from the global become that zone's
custom settings, and everything else keeps following the global.

## One set of settings, shared with the official app

Both apps read and write the same settings on the mower — the global config and each zone's own
config — and the last save wins, per zone. Until now a global cut height, mowing speed, blade speed
or stripe angle saved in the Toolkit stayed in the Toolkit: the official app kept showing the old
global, and mows started from the app or from the mower's own schedule used it. Those now reach the
mower's global config. In the other direction, a global changed in the official app is picked up by
the Toolkit the next time the mower sends its map, and the event log notes it.

## Resume after a power cycle

Swapping the battery in the yard restarts the mower with its job still open. The official app
offers Resume; the Toolkit offered only Start mow, which begins the job over. The Toolkit now shows
▶ Resume (on the main button and the Mow-on-hold card) and continues the mow. This one is built
from the report rather than a capture of the swap, so if Resume does not appear after your next
swap, please send the event log.

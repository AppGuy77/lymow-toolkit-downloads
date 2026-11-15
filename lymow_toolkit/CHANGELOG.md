Lymow Toolkit v2.14.11

The RTK pause, reworked from a field report: it pauses when RTK is lost, lets a mower out of a shed, gives way to your Resume, and no longer fills the screen with alerts. It keeps your sign-in, settings, maps, layout and history — just update.


- **Pause on RTK loss** — pauses when RTK is lost; the precision limit is its own switch.
- **Docks in a shed** — the drive out from the dock is not paused before the first good fix.
- **Your Resume wins** — a Resume from either app stands the RTK pause down until RTK is good again.
- **Quieter alerts** — no false "could not be sent"; a repeated alert shows once with a count.


## New

- **Pause on RTK loss pauses when RTK is lost** — no fix, or plain GPS — exactly what the switch means in the official app. Pausing while RTK is still present but its precision is worse than your limit is a new switch under it, **Also pause on poor precision** (Map → 🛰 Precision heat ⚙️). It is off by default; if you had changed the limit from 0.10 m it stays on. A limit saved to a zone or channel always applies there.
- **Docks in a shed or garage:** the RTK pause no longer stops the mower on the map's docking channel, or on its way out from the dock until the first good fix of the mow — no setting needed. **Skip near the dock** still adds a distance of your own, and a limit you saved on the docking channel still applies.
- **A Resume beats the RTK pause.** Resume the mower — in the official app, another Toolkit or this one — while the RTK or link pause is holding, and that pause stands down instead of pausing it again. It watches again once the signal has been good, or the mower is back on its dock.
- **Changes to the pause guards' settings are in the event log**, with the old and new value.

## Fixed

- **An RTK or link pause that reached the mower should no longer show "A command could not be sent."** When the cloud is slow to confirm (for example with the official app open on the same account), the mower's own Paused state is taken as the answer, and the pause is resumed when the signal returns.
- **The same alert repeated shows once, with a count** (×3), instead of filling the screen.
- **Pause on RTK loss should no longer switch itself off and back on** as the mower heads home or docks.
- **No "Precision guard held a pause" lines while the mower is charging** or otherwise not out mowing.

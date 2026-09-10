Lymow Toolkit v1.56.4

Everything below is a change from v1.56.3.


- Fixed: the mower should no longer pause itself for no clear reason while mowing. When it bumps something and backs up to work itself free (its "stuck — escaping" move), the Toolkit now gives it 30 seconds to get out on its own before pausing, the way the official app does. Before, it could pause the instant that move started and leave the mower parked with no fault shown and no notification from the Lymow app — most often where the RTK signal is weak. A mower still stuck after that is paused as before.
- Fixed: leaving remote control no longer pauses a mow that was never under remote control.
- New: the event log now names what paused the mower — the reason for each pause the Toolkit sends, or plainly that it was not the Toolkit — and names who sent every command.


## Random pauses while mowing

"Stuck — escaping" is the mower's own move: it has bumped something, and it backs up, turns and tries
again, usually freeing itself within seconds. The Toolkit used to pause it the instant that move began.
With auto-resume off, or the "stuck" fault excluded, the mower then sat paused with no fault code and no
notification from the Lymow app until someone pressed Resume — "random pauses", worse where the RTK
signal is weak and the mower veers and slips more.

The Toolkit now gives the mower 30 seconds to work itself free before the resistance rule pauses it, the
way the official app does. A mower that is still stuck after that, or one reporting a real stuck or jam
code, is paused at once as before. The event log records each move: "working itself free", then either
the mower freeing itself or the pause.

A second cause is fixed too: leaving remote control paused a mow even when the mower had never been under
remote control — a step that only meant to make sure it was out of remote mode. It now pauses only a
mower that was actually in remote control. Stopping the blades from the camera view still pauses, as before.

## The event log now says what paused the mower

A "Mowing paused" line used to name nobody, and the Toolkit's own pauses left no record of which part of
it sent them — so a "random pauses" report could not be answered from the log. Now every pause the Toolkit
sends is labeled with its reason (the resistance rule, a fault, the RTK or link guard, auto-resume, low
battery, or leaving remote control), and a pause with none of those behind it says plainly it was not the
Toolkit: the official app, Home Assistant, or a second Toolkit on the same account. Every command in the
log also names who sent it.

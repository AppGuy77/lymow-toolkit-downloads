Lymow Toolkit v1.51.6

Everything below is a change from v1.51.5.


- Multi-pass should now survive a recharge on big zones: a mid-pass recharge dock was read as "pass finished", so the next pass was sent to a dead battery and the run quietly ended after one pass.
- The recharge decision now uses YOUR return-to-dock level (Auto-recharge setting), not a fixed 20%.
- The dashboard and event log now say what a multi-pass run is doing at a recharge: "Pass 1 of 2 on hold — recharging".


## Multi-pass on zones bigger than one charge

On a zone that needs more than one battery charge per pass, the mower docks mid-pass to recharge —
normal behavior. The Toolkit misread that dock as the pass being finished and dispatched the next
pass within seconds, while the battery was empty. The low-battery protection canceled that start,
the mower later recharged and finished the interrupted pass on its own, and the multi-pass run
quietly ended after a single pass (field report, 2026-08-25 — thank you for the detailed logs).

The Toolkit now reads the mower's own job state, which distinguishes "docked to recharge, job
still open" from "job finished". A recharge dock holds the current pass: the mower charges,
resumes, and finishes it, and the next pass is sent only when the pass genuinely ends. If
Auto-recharge & resume is turned off on the mower, the run waits and the dashboard says so
instead of pretending the pass completed.

## Your recharge level, not ours

Whether a trip home is a real recharge or just the end of a pass is now judged against the
return-to-dock battery level you actually set (Auto-recharge in the Toolkit, or the official
app — default 20%), instead of a hardcoded 20%. If you raised your return level, a dock at a
higher battery percentage is now correctly treated as a recharge.

## You can see what it is doing

During a mid-pass recharge the Overview shows "Multi-pass · Pass 1 of 2 on hold — recharging,
resumes after charging". The event log records each boundary decision: when a pass is held
because the mower's job is still open, and when a pass genuinely completes and the next one is
sent. If a multi-pass run ever surprises you, the event log now tells the story.

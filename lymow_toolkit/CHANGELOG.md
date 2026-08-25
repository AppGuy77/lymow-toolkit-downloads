Lymow Toolkit v1.51.5

Everything below is a change from v1.51.4.


- The mower's light now stays on when you turn it on: the Toolkit's own background cleanup was switching off lights it didn't realize a person had asked for — a tap could flash the light on and it went right back off.
- "Drive at night with lights" should now actually keep the lights on during night mowing, and a manual tap always wins over the schedule.
- The event log now records who touched the light — your tap, the night-light schedule, Home Assistant, or the mower itself.


## Your light stays on

Tapping the light in the camera or remote view could flash it on and something immediately turned
it back off, while the button still showed it as on. The cause was the Toolkit itself: a background
cleanup, built to switch off a light that an old bug left burning, was also switching off lights it
simply had no record of — a tap made from another Toolkit install, from the official app, or a tap
it forgot after a restart. That cleanup now acts only on the one specific fault it was built for
(the mower reporting the old stale light flag) and never touches a light in any other situation.

## Night lights that stay on

The "Drive at night with lights" schedule was turning the lights on during night mowing — and the
same cleanup was turning them back off seconds later, so it looked like the schedule never worked.
On top of the fix above, the schedule's own behavior around your taps is reworked: a manual tap now
wins until the schedule next changes state (for example, the next mow entering the night window),
instead of being overridden 15 minutes later. Brief status flickers during a mow can no longer
strobe the light, and the schedule no longer endlessly retries a failed command against you. On
Home Assistant installs, the protection window for the mower's own built-in night light (set in the
official app) is now evaluated in your Toolkit time zone instead of the container's clock.

## The light is accountable

Every light on/off command now lands in the event log (Advanced Data tab) with what sent it — your
tap, the night-light schedule, or Home Assistant — and a light that changes with no Toolkit command
behind it is logged as changed by the mower or another app. If a light ever surprises you again,
the answer is one log line.

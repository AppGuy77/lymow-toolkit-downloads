Lymow Toolkit v1.50.2

Everything below is a change from v1.50.1.


- Camera improvements to reduce latency — the live camera is much more responsive on every platform, including inside Home Assistant — and the download is about 137 MB smaller.
- New: if an interrupted mow is still stored on the mower (why a mower can "start mowing on its own"), the Toolkit shows a banner and lets you cancel it, confirmed by the mower.
- Fixes for: cross-cut paint, zone settings saving everything as custom, mowers stuck at "connected (idle)", and Home Assistant setup on large installs.


## Camera

**Camera improvements to reduce latency.** The live camera is much more responsive — on Windows,
Mac, Linux and Docker, and inside Home Assistant too. The WiFi/4G choice is unchanged, the download
is about **137 MB smaller** on every platform, and the camera now reconnects on its own when you
return to a window it had stopped in to save data. The Start/Stop camera button always reflects the
real camera state.

## Mowing

**Leftover-mow banner.** The mower keeps its mowing job in its own memory — docking, from any app or
a fault, does not cancel it, and the mower can take itself back out later to finish it. That stored
job is why a mower can "start mowing on its own" with no command and no schedule. The Toolkit now
shows a banner whenever an unfinished mow is stored while the mower is docked or idle, and lets you
cancel it with one tap — confirmed by reading the mower back.

**The event log names who sent every command** — you, a schedule, or Home Assistant — and flags any
mow the mower started by itself.

**Cross-cut paint fixed.** The first pass should no longer turn the cross-cut color; orange should
appear only when the crossing pass actually starts.

**Zone settings fixed.** Changing one zone setting should no longer mark every setting as a custom
override — only what you actually changed is saved, the way the official app does it.

## Connection

**Mowers stuck at "connected (idle)"** that never went live should now connect on their own — and
opening the page forces a fresh connection attempt immediately.

## Remote

**The Remote deck height follows the mower's state.** Mowing shows the mow height, returning
through channels the channel height, docked the maximum (the mower raises its deck on the dock),
and paused whatever it was doing before the pause. Starting the remote camera also sets the deck to
that height so it matches. Moving the slider changes the deck as soon as you let go, and the
optional **"Remember my Remote settings"** switch uses your last applied remote height instead
(never while a mow is running).

## Home Assistant

The old separate **camera entity** and **Camera on/off switch** are retired — the live camera lives
in the Toolkit panel; updating removes the old entity for you. **Set up Home Assistant** should no longer
fail on large HA installs.

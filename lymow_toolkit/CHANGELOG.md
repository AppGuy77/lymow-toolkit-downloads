Lymow Toolkit v1.60.0

Everything below is a change from v1.59.5.


- **Lights you can trust.** The light button shows what the mower itself reports. A tap is held until the mower's own later report agrees; if the mower drops the command the Toolkit re-sends it, up to three times, before showing the mower's state and saying so in the event log. While charging on the dock the mower keeps its light off, and a tap then says so instead of flashing the lamp. After a tap the light should no longer flicker on and off.
- **The night light lives on the mower.** Drive at night with lights is now the mower's own Headlight Mode, written to the mower and read back, so it runs with the Toolkit closed. New: **Sunset to sunrise**, computed every day from the mower's position.
- **An RTK base per map.** Every saved map records the RTK base it was made with; restoring it, or reaching it in a multi-map run, binds that base and waits for the RTK link before mowing. Several bases, one property, one run.


## Lights

The round 💡 button — on the camera and now next to the mower's status on the Overview — shows what the
mower itself reports. Your tap is held until the mower's own later report agrees. If the mower drops the
command, the Toolkit re-sends it every 10 seconds, up to three times, then shows the mower's state and
writes the reason to the event log. Quick taps end where your last tap left it, and the button pulses while
a command is on its way. A dashed button means the mower has not reported its light yet and is being asked.
The mower lights itself on every trip back to the dock; the Toolkit never turns that off, because the mower
needs the light to see the dock. While the mower is charging on the dock it keeps its own light off, so a tap
then answers "Lights stay off during charging" instead of sending the command; on Waiting, while mowing and in
remote control the light works.

## Night light

**Drive at night with lights** is the mower's own Headlight Mode, the same setting as in the Lymow app. The
Toolkit writes the window to the mower, checks that the mower took it, and the mower runs it by itself with
the Toolkit closed. **Fixed times** are converted from your time zone to the mower's UTC clock on the day they
are written, and rewritten when daylight saving changes them. **Sunset to sunrise** computes the window every
day from the mower's position, with a **Margin** of extra minutes on each side for dusk and dawn. Lights still
come on only while the mower is working inside the window. The line under the schedule shows what the mower
actually holds, in your time. Turning the schedule off clears only a window the Toolkit wrote.

## RTK base per map

Every saved map records the RTK base station it was made with. When a map made with a different base is
restored — by you, or by a multi-map run at each map switch — the Toolkit binds the mower to that base with
the same command the Lymow app sends when you pair a base, waits for the mower to confirm it, then waits for
the RTK link before any mow starts. If the mower refuses, a multi-map run stops and says why; a manual restore
reports it and the mower stays on its current base. The backup list shows each map's base and the one bound
now.

## Overview

WiFi and 4G share one status card: the WiFi line (strength, network, address) with the 4G line under it.

Lymow Toolkit v1.50.3

Everything below is a change from v1.50.2.


- Fixed: a zone's custom settings could be silently erased when a mow started — a custom-angle zone would mow with the global pattern instead. Mow-start writes now carry the zone's complete configuration, and the event log proves what was sent and what the mower kept.
- Cross-cut mows should now paint the crossing pass in its own color, from the moment the angle changes — small zones included.
- Fixed: mowers could go silent after startup (no telemetry, no map, stuck on "connected (idle)") until you restarted — most visible in Home Assistant.
- Fixed: mows scheduled in the Toolkit never started. They work again — check your schedules, forgotten ones will now fire.
- Wi-Fi camera always falling back to 4G? Your router must allow multicast — turn ON both multicast routing and IGMP Snooping. The Toolkit now says this on screen, and tells you separately when the signal is simply too weak for video.


## Zone settings and mow start

Saving a zone stored your settings correctly — but starting a mow could wipe part of them off the
mower. The mower replaces a zone's stored settings wholesale, so a partial write at mow start
erased whatever it didn't mention: a zone set to mow at a specific angle would silently fall back
to the global pattern. Every zone write now carries the zone's complete configuration, the event
log shows a readable "Zone settings sent" entry with everything in it, and a read-back confirms
"Zone settings confirmed on the mower."

If a zone of yours has been mowing with the wrong pattern: open that zone's settings and press
Save once after updating — the full configuration lands on the mower and stays.

## Cross-cut painting

The crossing pass should now paint in the cross-cut color from the moment the mower changes angle
and starts its second direction — on small zones too, where it previously never triggered. The
split between the base color and the cross color lands at the true boundary. The color can trail
the mower by a few seconds; that is the mower recomputing its own mowed-area report, not the
Toolkit. And if the color ever doesn't appear, the event log now records the exact reason as a
`cross_claim` entry — include it when you report a problem and the diagnosis is one line.

## Mowers going silent

A mower could connect and then never send anything — no telemetry, no map, stuck on "connected
(idle)" — until the Toolkit was restarted. It happened when two parts of the Toolkit connected to
the same mower at the same moment, most often on Home Assistant. Fixed, and it now heals itself if
it ever loses its stream.

## Scheduled mowing

Mows scheduled **in the Toolkit** were not firing. They fire again — so check your schedules
before this update, because ones you forgot about will now run.

## The Wi-Fi camera and your router

The Wi-Fi picture goes straight from your phone or PC to the mower, and the two find each other
using **multicast**. A router that blocks it makes the Wi-Fi camera impossible — in the Toolkit
*and* in the official Lymow app — while 4G keeps working. Turn ON **both** *multicast routing*
(usually LAN → IPTV) and *IGMP Snooping* (usually Wireless → Professional), and keep the mower on
the same network as your phone, not a Guest network. Instead of "mower not reachable on WiFi", the
Toolkit now names this on screen — and a mower whose Wi-Fi reads -75 dBm or weaker gets the
different, correct message: the signal itself is too weak for video, and no router setting fixes
that one.

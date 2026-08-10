Lymow Toolkit v1.47.1

Everything below is a change from v1.47.0.


- Fixed: a mow without a cross-cut could paint part of the map in the cross-cut color, turning green trail orange behind the mower.
- Cutting parameters is now one panel, Mowing settings, with a single Save all settings button.
- Apply to mower is gone: the mower does not change a mow already running for any of these settings, and the app no longer claims it does.
- Blade speed is four buttons — Eco, Standard, Power, Turbo — with the one you are set to highlighted.


## Changed

**One panel, one Save button.** Cutting parameters was split into two groups — "live settings" with an
**Apply to mower** button, and "map settings" saved for later. The split described a distinction the
mower does not make. Whichever button you pressed, the machine stored the setting and used it from the
next mow; nothing in that panel has ever changed a mow already in progress. The panel is now
**Mowing settings**, and **Save all settings** keeps everything in it: cut height, mowing speed, path
spacing, blade speed, mow pattern, cut angle, cross-cut, mow order, perimeter laps and direction,
no-go laps, obstacle detection, edge following, outer discharge and channel travel.

To change how the mower is cutting right now, stop the mow, save your settings, and start it again.

**Blade speed is four buttons.** Eco, Standard, Power and Turbo sit across the panel with the one you
are set to highlighted, instead of a dropdown that hid three of the four behind a click.

**A more usable order.** Path spacing moved up next to cut height and mowing speed, where you compare
them; channel travel moved to the bottom of the panel under its own heading, since it is about
crossing between zones rather than about cutting.

**The mow pattern saves with everything else.** It had its own Set button, which could only work with
the mower idle. It is now part of Save all settings.

## Fixed

**A mow without a cross-cut could turn orange.** The cross-cut color added in v1.47.0 decided a
crossing sweep had begun from the mower's own area figures alone, without checking whether the zone
was set to cross-cut at all — so an ordinary pass boundary, such as moving from the interior to the
perimeter laps or on to the next zone, could start it. Because the starting moment is worked out
backwards from those figures, it recolored trail that had already been painted green, which is why
it appeared behind the mower some time after the grass was cut. The crossing color is now used only
where a crossing sweep can actually exist. Existing wrong orange clears when you update; your
coverage is not affected.

**The help text told you things that were not true.** The panel heading, the section headers, the
save hint, the channel-travel help bubbles, the blade-speed help and two entries in the in-app
glossary (📖) all described settings taking effect on a running mow. They have been rewritten to say
what actually happens.

**A settings message now matches the official app exactly.** The message the Toolkit uses for cut
height, mowing speed and blade speed carried two extra fields the official app does not send. It is
now byte-for-byte the message the app sends. This is the message used at mow start and by scheduled
mows.

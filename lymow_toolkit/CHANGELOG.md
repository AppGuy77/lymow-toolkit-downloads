Lymow Toolkit v1.50.1

Everything below is a change from v1.50.0.


- Fixed: in Home Assistant, the mower, dock, and RTK station icons were missing from the map — they now show.


## Fixed

**The map icons are back in Home Assistant.** When the Toolkit runs as a Home Assistant sidebar
panel, the mower, dock, and RTK station markers on the map were blank. They now display correctly.
The same fix also restores the **Download maps** button inside Home Assistant.

Only affects the Home Assistant panel — every other install (Windows, Mac, Linux, Docker) already
showed the icons and is unchanged.

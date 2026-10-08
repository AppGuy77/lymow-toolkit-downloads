Lymow Toolkit v2.10.6

A remote-control fix. It keeps your sign-in, settings, maps, layout and history — just update.


- **Driving should resume after a "picture is behind" pause** once the camera picture has been back under a second for a full second — in the Remote tab and the camera window.


## Remote control

- When the camera picture falls more than a second behind, driving and the blades still wait. Driving should now resume once the picture has been back under a second for a full second. Before, the picture had to get under 0.7 s, and a phone whose picture stayed just under a second — most often on WiFi through the Toolkit away from home — could stay paused.
- Each pause and resume is recorded in the downloadable event log, with how far behind the picture was.

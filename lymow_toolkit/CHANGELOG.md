Lymow Toolkit v2.10.4

Processor, remote-control and camera fixes, and security patches, for everyone on v2.10.3. It keeps your sign-in, settings, maps, layout and history — just update.


- **No more processor core stuck at 100%** — after a network drop the Toolkit should go back to idle on its own.
- **The arrow keys only drive:** a focused drop-down, slider or the map no longer takes them, and the camera window now drives its own mower.
- **A late picture pauses driving on every link** — 4G and WiFi direct too, not only WiFi through the Toolkit.
- **The camera says why it did not start** and tries the next way at once.
- **Security patches.**


## Processor and memory

- One processor core should no longer stay busy at 100% after a network drop. It was seen 1–2 hours after a restart, most often in Docker; the Toolkit should now go back to idle on its own.
- Long-running installs should stay lighter: queued notifications, the Home Assistant link and mowers you stop watching no longer hold memory, and fewer requests go to the cloud.
- The + / − controls in the RTK and dock-grace settings no longer re-send an older value when you click elsewhere on the
  page, and a hidden tab no longer pulls the mowed-area trail every few seconds.
- A streamed Google sign-in that is left open closes on its own.

## Remote control

- The arrow keys only drive: with the camera on, a focused drop-down, slider, number box or the map no longer takes them, and without a live picture they do nothing.
- The camera window (the 📷 on the map or the Overview) now drives its own mower with the arrow keys. The first press asks the arrow speed inside the window; closing the window or switching its mower while a key is held stops that mower.
- A 4G or WiFi-direct picture more than a second behind now pauses driving and stops the blades until it catches up, as WiFi through the Toolkit already did — in the Remote tab and the camera window.
- **Keep camera on** ends about 5 minutes after the page that switched it on is closed.

## Camera

- When the mower's camera cannot start, the reason is shown (for example "that mower is not connected right now") and the next way is tried at once, instead of after 25 seconds.
- The WiFi picture moves to the mower's direct link only when that link is no further behind, and goes back if it falls behind.
- On Android, Mac and Linux browsers the WiFi picture should no longer jump backward.

## Installs

- **Docker:** finished helper processes are cleaned up.
- The settings snapshots kept before each change are capped at 100 per mower; older ones are removed.
- **macOS:** starting the Toolkit by hand from Terminal now needs `sudo`. Running `sudo bash install.sh` again may move the Toolkit to `/usr/local/lymow-toolkit`; your sign-in, settings and maps come along.
- **Security patches.**

## Languages

- The new texts are translated.

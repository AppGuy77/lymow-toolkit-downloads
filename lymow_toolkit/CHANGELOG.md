Lymow Toolkit v1.54.2

Everything below is a change from v1.54.1.


- Your settings now save: since v1.52.0, settings you changed (language, units, time zone, map style, trail/cross-cut/heat-map colors, night light) were kept only by the browser you changed them in and never saved on the server, so they didn't follow you to another browser or phone and the log filled with "[state] update aborted, nothing written". They now save, and a failed save is reported instead of being called a success.


## Your settings now save

Every setting the Toolkit shares across your browsers and devices — the **language**, **units**,
**time zone**, **map style** (satellite/street/custom tiles), the **trail**, **cross-cut** and
**heat-map colors**, and the **night light** switch — is saved on the server so it follows you from your
computer to your phone. Since v1.52.0 that save failed every time: the Toolkit answered "saved", the
browser you were in kept its own copy so it looked fine there, but nothing reached the server. On another
browser or phone the setting was back to the old value, and the server log showed a line of
`[state] update aborted, nothing written: UnboundLocalError` for every change.

That's fixed: settings save again, and if a save ever fails the Toolkit now says so instead of reporting
success. After updating, set anything that didn't stick once more and it will follow you everywhere.

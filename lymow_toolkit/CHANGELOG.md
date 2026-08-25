Lymow Toolkit v1.51.4

Everything below is a change from v1.51.3.


- The live camera on Windows should no longer turn green: over a plain http:// address the WiFi picture was handed to a Windows decoder that corrupts this stream — the camera now switches to 4G with the reason shown, or explains how to get the WiFi picture.
- The live picture should no longer shrink into the right edge of the screen: when the direct WiFi link failed, the fallback left debris on screen that squeezed the picture into a small box beside a black area.


## No more green picture on Windows

Viewing the Toolkit from a Windows browser over a plain `http://` network address (for example
`http://192.168.x.x:8787` from another computer), the WiFi camera picture could arrive solid green
with blocky noise. On that kind of page the browser cannot use the Toolkit's software video
decoder, and the remaining playback path hands the stream to a Windows hardware decoder that is
known to corrupt it. The Toolkit no longer shows that broken picture: on the Auto camera link it
switches to 4G and says why on screen, and on WiFi-only it explains the two ways to get the WiFi
picture — open the Toolkit on the machine it runs on (localhost), or use the secure remote link.
Phones, Macs, and Linux browsers are unaffected.

## The picture no longer shrinks into a corner

When the direct WiFi camera link failed and the camera fell back to streaming through the Toolkit,
the failed attempt's video surface was left on screen. The live picture then appeared squeezed
into a small box against the right edge, next to a black area. The fallback now removes the failed
surface before showing the live one, on both the Remote tab and the Overview camera popup, on
every platform.

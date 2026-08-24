Lymow Toolkit v1.51.2

Everything below is a change from v1.51.1.


- Remote control away from home works again: through your away link, the joystick and the fullscreen driving controls should now unlock as soon as the live picture arrives (they stayed disabled even with live video).
- On phones, the camera now uses your phone's true fullscreen — the browser's bars disappear when you rotate to landscape. If the phone drops fullscreen (keyboard, notification, a swipe), a centered ⛶ button should bring you straight back.
- If the live picture dies mid-session, the blades stop, the reason appears on screen, and on Auto the camera reconnects by itself.


## Remote control away from home

v1.51.0's away-from-home camera shipped with a gap: a viewer on the away link got live video, but
the joystick stayed locked and the fullscreen driving controls never appeared. Every camera path —
at home, through the Toolkit relay, and iPhone's player — now arms the same controls the moment
the picture is live: joystick, fullscreen button, mini-map, light, and deck sync.

## True fullscreen on phones

Rotating to landscape (or starting the camera in landscape) now asks the phone for real
fullscreen, so the browser's tab and address bars disappear instead of just filling the page.
Android grants it on the rotation itself; iPhone may ask for one tap — your first touch of the
joystick is enough. Phones lose fullscreen easily (keyboard, notifications, an accidental swipe),
so whenever that happens a centered ⛶ Full screen button appears on the picture — one tap
returns. Desktop is unchanged.

## A dying picture is handled, not frozen

If the relayed live picture stops mid-session, the Toolkit now stops the blades immediately,
says on screen what happened, and on the Auto camera link reconnects by itself instead of
freezing on the last frame. On iPhone, the blade safety gate now also rides on video the Toolkit
itself delivers, which should end spurious "camera required" blade stops during brief buffering.

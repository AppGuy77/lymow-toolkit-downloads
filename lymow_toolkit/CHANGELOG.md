Lymow Toolkit v1.51.3

Everything below is a change from v1.51.2.


- The camera's ⛶ fullscreen button now works on computers: on a desktop browser it was hidden underneath the camera-link (Auto/WiFi/4G) buttons, so there was no visible way into fullscreen without rotating a phone.
- Exiting fullscreen now sticks: pressing ✕ Exit used to throw you straight back into fullscreen — it now stays out until you rotate the phone again or tap ⛶ yourself.
- Every fullscreen button is now the simple ⛶ symbol, and the return-to-fullscreen button sits centered on the picture — it no longer covers the camera-link buttons.


## Fullscreen works on computers again

On a desktop browser, the remote camera's ⛶ fullscreen button has been hidden underneath the
camera-link (Auto/WiFi/4G) buttons since v1.47 — phones could still enter fullscreen by rotating,
but on a computer there was no visible way in at all. The camera-link buttons now appear only in
fullscreen (where they belong), and the ⛶ underneath is visible and clickable again. Verified by
an automated screen-layout sweep across desktop and phone, camera view and remote, windowed and
fullscreen: no control covers another anywhere.

## Exiting fullscreen sticks

Pressing ✕ Exit bounced you straight back into fullscreen: leaving fullscreen triggers the same
checks that rotation does, and with the phone still sideways they immediately re-entered. An
explicit Exit now stays out until you rotate to portrait and back, or tap ⛶ yourself. The camera
still opens in fullscreen the way it always has — Exit is simply respected now.

## One clean ⛶ everywhere

Fullscreen buttons showed spelled-out labels, and the camera view could show two different
fullscreen buttons at once — one of them sitting on top of the Auto/WiFi/4G selector. Every
fullscreen control is now the bare ⛶ symbol, the return-to-fullscreen button sits centered on the
picture where nothing else lives, and only one fullscreen control is ever visible at a time.

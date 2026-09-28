Lymow Toolkit v2.8.2

An update for everyone on v2.8.1. It keeps your sign-in, settings, maps and history — just update.


- **An expired Lymow sign-in should show the sign-in screen** instead of leaving the Toolkit on "offline" — at home and through the away link. With **Stay signed in** it signs you back in by itself.
- **Remote control is safer.** Switching mowers stops the camera and blades first, a page that disappears mid-drive should have its mower stopped within a second, and a mower left in remote control is taken out of it (paused, never canceled).
- **The Remote says why the joystick did not move the mower**, in the middle of the screen.


## An expired sign-in asks you to sign in again

Lymow's sign-in lasts about a month from the day you signed in, and nothing can extend it. When it ran out, the
Toolkit could sit on "offline" or "asleep" — or show "could not connect" — instead of asking you to sign in again, and
it kept asking the Lymow cloud with the finished sign-in. It should now show the sign-in screen, with your email filled
in and the right sign-in button (email, Google or Apple), and stop asking the cloud until you sign in.

This works through the **away link** too: open your away address, sign in there, and everything carries on at the
same address. Google and Apple sign-in open inside the page.

With **Stay signed in**, the Toolkit should sign you back in by itself whenever the sign-in runs out — not only after a
restart — and the event log says so ("🔑 Lymow sign-in renewed with your saved password"). If Lymow refuses the saved
password (it was changed somewhere else), the sign-in screen appears and the old password is forgotten.

## Safer remote control

- **Switching mowers.** Picking another mower while the Remote camera is live should first stop the camera and the
  blades and take the first mower out of remote control, so the joystick can never drive one mower on another
  mower's picture.
- **A page that disappears mid-drive.** If the tab is closed, the phone locks or the network drops while you hold the
  joystick, the Toolkit should stop the mower itself within a second. The event log says "🛑 Remote control: the mower
  was stopped — the page driving it went quiet".
- **Left in remote control.** A mower the Toolkit put in remote control, with the blades off and nobody driving it or
  watching its camera, is taken out of remote control after about a minute — a running mow is paused, never canceled.
  Remote control started from the official app is never touched.
- **Other tabs.** Moving between the other tabs no longer takes a mower out of remote control; leaving the Remote tab
  still does.
- **Refusals are said.** When the mower did not move — no live picture, or the cloud link not responding — the reason
  appears in the middle of the screen, also in fullscreen.
- **Home Assistant.** Closing the page on the Home Assistant remote card or panel should stop the blades at once, and
  the remote card shows which mower the camera belongs to and the signal read-out.
- **Fleet Mode.** The Remote follows its own mower: the deck height set when its camera starts, the Dock choices and
  "Remember my Remote settings" use the mower you are driving, not the one on the dashboard.

## Other fixes

- macOS: the desktop app opens the port your install uses, and the README's links and uninstall steps are correct.
- Translations: the Home Assistant area is named "Lawn" in every language, matching what Home Assistant shows.

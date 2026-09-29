Lymow Toolkit v2.8.3

An update for everyone on v2.8.2. It keeps your sign-in, settings, maps and history — just update.


- **Remote control should keep up with you.** The delays came from stacked commands and from codec conflicts with iPhone — the joystick and the picture should now respond right away.
- **Two joysticks on phones and tablets**, and a fullscreen camera that fits every screen — nothing under a phone's camera cutout.
- **A charging mower can no longer fill the log**, and logs, old Docker images and leftover files are cleaned up.


## Remote control keeps up

Remote control could fall seconds behind: stacked commands caused increased delays, and codec conflicts with iPhone
held its picture back. The joystick and the picture should now respond right away — on your home WiFi, on 4G and
through the away link — and the iPhone gets the live picture.

When the camera picture falls behind anyway (a weak connection), driving and the blades wait until it catches up, and
the screen says so. You never drive on an old picture.

## Two joysticks on phones and tablets

Remote → **Controls**: **Two joysticks** (the default on a touch screen) — the left stick drives forward and back, the
right stick turns, and holding both drives an arc. **One joystick** is the round stick you know; a computer uses it by
default. **Controller size** is now saved for each kind of device, so resizing on the phone never changes the computer.

## Fullscreen camera

- **Phones** should go truly fullscreen (no browser bars) and show the landscape layout even when held upright. ✕ Exit
  on a phone also turns the camera off.
- **Computers** should go into real browser fullscreen when you press ⛶, or with your first click when the camera
  filled the window by itself. Esc leaves fullscreen and stays out.
- **Nothing in the way.** No button sits in the middle of the picture, and on a phone no control sits under the camera
  cutout, the rounded corners or the home bar.
- **Sized to your screen.** The camera screen's buttons and read-outs follow your screen's size.

## The light button tells the truth

When the mower keeps its light off while it is on the dock, or outside its own headlight window, the 💡 shows off — and
the Toolkit stops re-sending the light.

## Less cloud use

A mower that has gone to sleep should stay asleep: the Toolkit's own background checks no longer wake it. The Toolkit
also no longer ends a remote-control session that the official app started.

## Logs and disk

- A charging RTK mower with the **Fully charged** notification on could fill the log without end. That should no
  longer happen, and a log that floods for any reason is now capped.
- Logs are capped on Windows and in Docker, and Docker removes old images after an update.
- Updates and uninstalls clean up files left behind by older versions.

## Also

- Error and event-log messages that still showed in English now show in your language.
- Security patches.

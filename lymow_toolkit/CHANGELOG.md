Lymow Toolkit v2.8.5

An update for everyone on v2.8.4. It keeps your sign-in, settings, maps and history — just update.


- **The camera should start about as fast as the official app** and should no longer keep reconnecting on WiFi.
- **Remote control, the camera and the 💡 should always act on the mower you picked**, and the 💡 should show the light the mower turns on by itself at night.
- **Each zone keeps its own settings, and the mower's zone settings are the truth** — no more "zones disagree".


## The camera

- **Faster on WiFi.** The WiFi picture now starts through the Toolkit, the way VLC opens the mower's camera, and should
  appear in a few seconds instead of up to 20 or more.
- **No more reconnect loop on WiFi.** The camera should connect once and stay. Opening the same mower's camera on
  another screen takes it over; the first screen says **On another screen · tap to take back**.
- **Straight to 4G when WiFi cannot work.** A mower that is on 4G because its WiFi gave it no working address goes
  straight to 4G in Auto. In WiFi only, the line under the picture says why, in a few words (**WiFi: no IP**, **WiFi: IP
  unreachable**). Settings → **Camera — signal levels** shows each mower's network.
- **Auto follows your Settings → Camera levels** on every WiFi picture, on the Remote, the camera window and every
  camera-grid tile; a grid tile on 4G comes back to WiFi at your return level.
- **Short status lines** under the picture.
- **The camera's mini-map shows the camera's own mower.**

## Remote control and the light

- **Every control should act on the mower it shows.** In Fleet Mode, with the camera window open on another mower, the
  Remote's picture, Pause, Dock, Clear Fault, 💡, blades and leaving remote control should all stay on the Remote's
  mower, and the camera window's on its own.
- **The 💡 should show the light as it is.** At night the mower turns its light on by itself in remote control (at a
  lower brightness); the 💡 should show it on, and off again when the mower turns it off after remote control.

## Zone settings

- **Each zone keeps its own settings.** With several zones selected, each shows and keeps its own custom settings;
  each setting shows **Mixed**, **Custom** or **Global**, and **↺ Use global** puts one setting back to the global.
- **Saving asks where:** **Update specified zones**, **Global** (clears every zone's custom settings) or **Keep custom
  settings** (the global changes, every zone keeps its own).
- **Mowing a customized zone asks how to cut:** each zone's own settings, the Global settings, or these Mower settings
  — just this time, or saved.
- **The mower's zone settings are the truth.** A change made in the official app shows in the Toolkit by itself; the
  "zones disagree" warning is gone.
- **Blade speed is saved on the mower for each zone**, and should no longer be changed during a mow.
- **Schedules:** **Schedule with specified settings** — on, the schedule's settings are used for that mow; off, the
  mower's own settings.

## Mowing data

- **Last finished mow** should be the mower's real last mow (the same one the official app's history shows), with
  when, zones, area mowed, time in hours and minutes and battery used; the map's size is shown separately.
- **Progress is the mower's own %**, and the time left is in minutes.
- **Fleet Mode:** every mower's status and map should be current without switching to it; a tile shows **Mow on hold**
  during a recharge break, and a multi-pass run shows its pass.
- **"Job complete" only when the job is complete**; otherwise **Job ended at N% — unfinished**.

## Notifications

- The set: **Mowing started** (with its zones), **Zone complete**, ONE message per trip to the dock (job remaining,
  complete, canceled or ended at N%), **Resuming job**, errors and warnings, manual action required, **Fully charged**.
  Lymow's own messages are not repeated.
- **Paused**, **Stopped in the yard**, **Error cleared**, **Toolkit updated** and **Multi-pass** are turned off
  once — turn any back on in Settings → **Push notifications**.

Lymow Toolkit v2.7.0 — the first official v2

This is the Lymow Toolkit for everyone from now on. If you are on v1 (1.60.x), your Toolkit offers it as a normal update and keeps your sign-in, settings, maps and history. If you are on the v2 Beta, it is the last release on the beta channel, which closes two weeks from now; after this update your Toolkit follows the official releases by itself (Windows, Linux, macOS). Home Assistant add-on and Docker users on the beta repository see a "Move to the official repository" line under the header with the link, until they are on the official one.


- **Push notifications with no app and no Home Assistant.** Settings → Phone Access & Notifications. On the phone, open the Toolkit from its away link, add it to the home screen (one tap on Android; two taps on iPhone, shown on the page) and press Turn on for this phone. iPhone: iOS 16.4 or newer. Android: Chrome, Samsung Internet or another Chromium browser.
- **Home Assistant is one switch.** Enable Home Assistant & automations sets everything up by itself, checks for conflicts first, and asks what to remove when switched off. An Install Mosquitto button appears when the broker add-on is missing.
- **31 short phone notifications**, each with its own switch, titled with the mower's name — no Home Assistant device or broker needed. One route at a time: Home Assistant app or browser push, and the switches are live.
- **The dashboard above the map.** Tap a tile to keep it (green outline); collapsed shows the kept tiles, per mower in Fleet Mode; camera and center-on-map beside each light.
- **Mower settings beside the map**, blade speed as four buttons, four folding groups under Cutting parameters, one Map settings container.
- **The away link verifies the relay's identity** on every connect and refuses anything else.


## Coming from v1

Everything the v2 betas brought is in this release: Fleet Mode (every mower on one map, fleet start / pause / dock, a camera grid, per-mower notifications, locations), a light button that shows what the mower itself reports, the night light stored on the mower with a sunset-to-sunrise mode, an RTK base remembered per map, the vector street map, Sign in with Apple, cut-angle rotation per mow, Plot on Error, and the camera relay. The wiki has a page for each. Your data carries over; nothing is reset.

## Push notifications (new)

Notifications on your phone's lock screen — Job started, Front lawn done, Docked, charging, Error — with no app to install and no Home Assistant. They go through the phone's own browser, which is free; the Toolkit sends each message encrypted for that phone only.

What the phone makers require, and the page checks for you:
- **A secure address.** Open the Toolkit on the phone from its **away link** (the mower-xxxx.lymowtk.cc address), not the http home address. A VPN does not change this.
- **The home-screen icon.** Android: press **Install on this phone**, one tap. iPhone: press **Show me how to add the icon** for the two taps (Share → Add to Home Screen), then open the Toolkit from the new icon; the switch unlocks by itself.
- **iPhone: iOS 16.4 or newer. Android: Chrome, Samsung Internet, Edge or another Chromium browser.**

Then press **Turn on for this phone**. Every phone in the list gets every message until you press Remove on it. Desktop browsers can receive them too, behind the Allow desktop browsers switch. A phone that clears its browser data or deletes the icon is dropped from the list by itself the first time a message cannot reach it, and the list says why. Send test sends one to every phone and reports what each answered. The phone names the sender "Lymow Toolkit"; the mower's name is the title.

One route at a time: turning browser push on turns the Home Assistant phone notifications off, and the other way round — the switches are live, no Save, and only the active route's Send test works.

## Home Assistant

One switch, **Enable Home Assistant & automations**, replaces Publish, Setup and Clear Data. Before switching on it checks for conflicts — the Lymow-HA integration, automations that already use Lymow, an MQTT integration pointed elsewhere, leftovers of a previous Toolkit install — and names them. On, it sets up the broker login, the MQTT integration, the Lawn area and the dashboard by itself; on the add-on with nothing else needed, elsewhere with the Home Assistant address and access token. Off, it asks what to remove: the mower devices and dashboards by default, Mosquitto and the MQTT integration only when nothing else in Home Assistant uses them. A switch left on from a previous install is checked and repaired at start.

On the add-on, when the Mosquitto broker add-on is missing, an **Install Mosquitto** button opens its page in Home Assistant; install and start it there and the switch comes alive by itself, no refresh. Push notifications no longer depend on the Home Assistant device: their switch stands alone. The remote-control card in Home Assistant is the Toolkit's own remote view, camera and joystick only; the MQTT drive buttons and the deck-height number are retired.

The notification catalog is 31 short messages: Job started (with the schedule's name), Resuming job: zone, zone done, Job complete with the totals and battery, Docking (with the battery), Docking to recharge, Docked, charging, Fully charged once per dock stay, Error with the fault's name, Emergency stop, Stuck, Lifted, Offline / Back online, Needs you with the reason, a pause the mower did not confirm, a Toolkit update. Each has its own switch. Leaving remote control sends nothing.

## Overview

The dashboard sits above the map, right under the tab strip. Expanded, every tile shows; tap a tile to keep it when collapsed, and the green outline marks the kept ones. Collapsed shows only the kept tiles as one compact strip — or just the title line when none are kept; the defaults never come back by themselves. The kept tiles are saved per mower on the server, so every browser shows the same strip; open or closed is remembered per device. In Fleet Mode every mower has its own row, with its own toggle, color, light, camera and center-on-map buttons; the camera button opens that mower's own popup, never the grid.

Mower settings — cut height, blade speed as four buttons, mowing speed, path spacing — live in their own column to the right of the map on a wide screen and under it on a phone; Apply saves them for the selected zones or globally and reads them back from the mower. Cutting parameters, Schedule a mow, Multi-pass and Adjust cut angle offset share one Cutting & scheduling box. Cutting parameters fold into Cut pattern, Obstacles, Perimeter and Channel settings; the map controls fold into one Map settings container. Each remembers its state per device. On the network bar, Away access and its status sit at the right edge.

## Remote

Blade speed is four buttons on their own line, with the status under them. A test notification is titled with the mower's name, like every real event.

## Away link

The Toolkit verifies the relay's SSH identity against a pinned key on every connect — the key the relay publishes, with the same key bundled as a fallback — and refuses anything else, shown as "Relay identity mismatch — refusing to connect". The Away access hover states what the connection is: one outbound SSH connection from this computer to relay.lymowtk.cc on port 2222, nothing listening inbound. The relay's fingerprint is on the wiki's Remote Access page.

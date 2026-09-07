Lymow Toolkit v1.56.2

Everything below is a change from v1.56.1.


- New: every phone notification has its own switch. Settings → Home Assistant → Phone notifications → Choose notifications… lists all 66 messages the Toolkit can push, each with an on/off switch, the exact text the phone shows, and a Test button for that one message. One list for the whole account, saved on the Toolkit.
- New: many more moments reach the phone — reaching a zone, progress milestones, the mow's totals, stuck, lifted, offline and back online, the emergency stop, and what the Toolkit did — with Pause, Resume, Dock, Cancel task and Clear error buttons on the notification.
- Fixed: phone notifications, their fault names, their action buttons and the example texts now arrive in the Toolkit's language, in all 15 translated languages. Before, the fault name stayed English.
- New: the mower's own messages (rain detected, charging abnormal, geo-fence lock, new firmware, its own scheduled start, docked due to an error) have their own rows, each in the group it belongs to.
- Fixed: with Log events switched off, only the safety guards reached the phone. Every notification is now sent whether or not it is logged.
- Fixed: the WiFi camera "via Toolkit" (away link, Nabu Casa, Home Assistant, iPhone) failed with "No usable temporary directory found" when the Toolkit computer's disk was full or read-only. The relay keeps its configuration in the Toolkit's data folder now, or runs with no file at all, and says why when it cannot start.
- Fixed: iPhone showed "Tap to start the live picture" on every retry when the relay had not started. The phone now asks the Toolkit first and shows its reason; the tap prompt is only for a real autoplay block.
- Fixed: Windows on a plain http page (Home Assistant on the LAN, http://<address>:8787) refused the WiFi picture with "Windows can't show the WiFi picture over plain http". It should now play over WebRTC through the Toolkit computer's port 8788; the Windows installer opens it, Docker Desktop users add the 8788 mappings.
- Fixed: turning the blades on in remote control (and other parameter changes) failed with "OSError: Read-only file system" when the Toolkit computer's disk could not be written. The command now goes out and says that no backup could be kept; the Apply result no longer overwrites an error with "sent — not confirmed".
- New: Advanced Data shows the Toolkit computer's data drive, live — free space with a red warning under 2 GB, and a READ-ONLY warning with what to do.
- Fixed: the Home Assistant add-on filled the disk, about half a gigabyte per update. The add-on now pulls the ready-made image and Home Assistant deletes the previous version on every update. Free the old images once with `docker image prune -a` from the Home Assistant console.


## Every phone notification has its own switch

**Settings → Home Assistant → Phone notifications → Choose notifications…** opens the full list of the 66
notifications the Toolkit can push — one row per message, not just the four groups (Mowing progress,
Docking & charging, Problems, Toolkit actions) — each with an on/off switch, the exact text the phone will
show in your language, and a **Test** button that sends that one message to your phones right now. All
on / All off per group, **Defaults**, and a search box; the count beside the button shows how many are on.
It is one list for the whole account, saved on the Toolkit, so every browser sees the same. A notification
is sent only when Push notifications is on, its group is on and its own switch is on; the Home Assistant
Events entity still fires for every event, for your automations.

## Many more moments reach the phone

Beside what v1.55 sent, the mower now reports reaching a zone and starting it, progress milestones you
choose (50 and 95 percent of the zone by default), the mow's totals when it finishes (zones, area,
minutes), paused in which zone, stuck and trying to free itself, lifted, offline for a minute and back
online, remote control, mapping, firmware updates, and the emergency stop. The Toolkit's own actions
are reported too: auto-resume after charging, a pause the mower did not confirm, a
guard that held a pause, multi-pass boundaries, a Toolkit update. **Pause, Resume, Dock, Cancel task and
Clear error** buttons ride on the notifications, as the moment allows, and run through the same command
path as the dashboard's buttons, so they need "Allow Home Assistant to control the mower". The
fully-charged level (98 percent by default) and the progress milestones are yours to set.

## Phone notifications in the Toolkit's language

The message on the phone, the fault names in it, the action buttons and the example texts in the list use
the language set in Settings, in all 15 translated languages, from the same translations the app uses.
Before, the sentence was translated but the fault name went out in English. The mower's own messages
(rain detected, charging abnormal, geo-fence lock, new firmware, its own scheduled start, docked due to
an error) have their own rows, each in the group it belongs to. And with **Log events** switched off,
only the safety guards reached the phone; every notification is now sent whether or not it is logged.

## The camera relay and the mower commands survive a full or read-only disk

The camera relay kept its configuration in the system's temporary folder; on a Home Assistant machine
whose disk could no longer be written, every relayed picture failed with "No usable temporary directory
found". It now keeps its configuration in the Toolkit's own data folder, or runs with no file at all, and
says why when it cannot start. The iPhone asks the Toolkit before it plays and shows its reason; "Tap to
start the live picture" appears only for a real autoplay block. Windows on a plain http page should now
get the WiFi picture over WebRTC through the Toolkit computer's port 8788, which the installer opens.
Turning the blades on (and other parameter changes) no longer dies with "OSError: Read-only file system":
the command goes out and the result says that no backup could be kept. **Advanced Data → Toolkit
computer** shows the data drive's free space, live, red under 2 GB, and READ-ONLY with what to do. The
Home Assistant add-on pulls its ready-made image instead of building on the box, and Home Assistant
deletes the previous version on every update; reclaim the images earlier versions left behind once from
the Home Assistant console: `login`, then `docker image prune -a -f`.

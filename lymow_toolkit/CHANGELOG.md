Lymow Toolkit v2.7.4

An update for everyone on v2.7.0 to v2.7.3. It keeps your sign-in, settings, maps and history — just re-download and install.


- **The mower should keep to its resume hours.** Settings → **Recharge & Resume** (it replaces Auto-recharge) is the official app's Recharge & Resume — the switch plus Start Time and End Time — with the Toolkit's own battery levels (5–95%). Saving the levels no longer clears the hours set in the official app, and the Toolkit only sends the mower back out after a charge inside those hours.
- **Home Assistant entities are named after the mower** (`sensor.johnny_5_battery`). Settings → Home Assistant → **Entity names** renames existing ones and updates the automations, scripts, scenes and dashboards that use them, after a backup.
- **Settings controls line up and show their whole text.**
- **Security patches.**


## Recharge & Resume

The Settings section that was Auto-recharge is now **Recharge & Resume**, laid out like the official Lymow app's: the switch, **Start Time** and **End Time** — the hours the mower may go back out to finish a mow after recharging — and the Toolkit's own **Return to dock at** and **Resume after charging to** levels (5–95%). The times show in your local time, converted the same way the official app does, and 00:00 to 23:59 means any time. What the panel shows is what the mower itself reports; saving waits until the mower has reported its setting, sends the whole setting, and then says whether the mower confirmed it.

Saving the battery levels in the Toolkit could clear the start and end times set in the official app — after which the mower could go back out at any hour. That should no longer happen. If your times look grayed out in the Lymow app, set them once more, in either app.

The Toolkit follows the same hours itself: after a charge it only sends the mower back out inside them. A mower you send home stays home — also after the Toolkit restarts or updates. Schedules and multi-map runs now wait while the mower is recharging in the middle of a mow instead of treating it as finished. And when another Toolkit or app keeps using the same Lymow account at the same time, the Toolkit stops starting or resuming the mower on its own and shows a banner until that ends; your own buttons still work. Run one Toolkit per account.

## Home Assistant entity names

The mower's Home Assistant entities are now named after the mower — `sensor.johnny_5_battery` instead of a device number. New entities get these names by themselves. Existing ones keep their names until you rename them in **Settings → Home Assistant → Entity names**: **Preview** shows every change first; **Rename now** saves a backup, renames the entities (their history moves with them) and updates the automations, scripts, scenes and dashboards that use them; anything kept in YAML files is listed with the exact change to make by hand. **Download** saves those items as they are now or with the new names, with an old → new list for search and replace, and **Restore / Update** puts a file back.

## Settings controls

Every text box, time and drop-down in Settings now fills its row and lines up on the same edge, so times like 10:00 AM and long options show in full. On a phone each label sits above its control.

## Security patches

This release includes security patches. Updating is recommended for everyone.

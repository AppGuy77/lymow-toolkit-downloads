Lymow Toolkit v2.14.0

Back up and restore your settings, Lymow One deck handling, and a Donate button. It keeps your sign-in, settings, maps, layout and history — just update.


- **Back up and restore your settings** — Settings → Back up & restore: every setting, the imagery alignment, the mowed paint and heat maps in one file, to move to another computer or platform.
- **Lymow One** — This mow only changes and the cut height after Recharge & Resume should now take effect.
- **☕ Donate** — a button at the top of the page opens the Toolkit's Ko-fi page.


## New

- **Back up and restore your settings.** Settings → **Back up & restore** has **Download settings**: one file with every setting you made — preferences, Warnings & errors, schedules, per-zone cut settings, the cut-angle offset, channel settings, locations, RTK base names, the satellite-imagery alignment and your Home Assistant choices — plus what the map shows: the mowed paint, the freshness record and the RTK and link heat maps. On another computer or platform (Windows, Mac, Linux, Docker or the Home Assistant add-on), install the Toolkit, sign in with the same method as before (your away address follows your account), and use **Restore from file**. The Toolkit shows what the file will change and whether its mowers are on this account, keeps a copy of your current settings (downloadable, so a restore can be undone), writes the file's settings and checks every value afterwards. Your sign-in, passwords and tokens are never in the file, and the ones on the new Toolkit stay as they are. Restore waits while a mower is mowing. Shut the old Toolkit down first: two Toolkits on one account compete for the away address.
- **☕ Donate.** A Donate button beside the 📖 glossary at the top of the page (a full-width button in the ☰ menu on a phone) opens the Toolkit's Ko-fi page in a new window. The Toolkit is free — donations are appreciated, never expected.
- **Lymow One: Same as cut height.** The channel settings on a Lymow One have a button that sets the channel deck height to your cut height.

## Fixed

- **Lymow One: This mow only changes should now take effect.** On a Lymow One a cut height or mowing speed change for the running mow only took effect after the deck had been lowered all the way in remote control. The Toolkit now lowers the deck first, then makes the change.
- **Lymow One: should go back to your cut height after Recharge & Resume.** A Lymow One came back from charging still cutting at the channel deck height. The Toolkit now re-applies your height once the mower is back inside the zone, clear of the channel.
- **Saving settings to all zones should no longer change your channel settings.** A global save set the channel deck height to 100 mm and the wheels up when the Toolkit had no channel settings of its own saved; it now keeps the mower's own channel values.

## Languages

The new section, the Donate button and the new messages are translated in all 15 languages.

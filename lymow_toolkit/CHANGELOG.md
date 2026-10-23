Lymow Toolkit v2.13.0

A table of every zone's settings, and a multi-pass fix for Do Not Disturb hours. It keeps your sign-in, settings, maps, layout and history — just update.


- **Every zone and every setting in one table** — Mowing settings → Table: compare zones, change several at once, drag to reorder.
- **The Mower settings column steps aside while the table shows** — the map and the table take the full width.
- **A catch-up mow should no longer be cut off by Do Not Disturb hours** — the next pass waits for them to end.


## New

- **Every zone and every setting in one table.** Mowing settings has a **Form / Table** switch. Table shows every zone as a row and every cutting setting as a column, with an **All zones** row on top. Change the cells you want and press Save: each changed cell goes to its zone, a change in the All zones row to every zone, and the mower confirms it. A zone's own value is marked green, an unsaved cell orange; the count of unsaved cells shows beside the switch, and Save writes them whether the table or the form is showing. The cross-cut angle shows only on a Chess Board row. The pick box in a row selects the zone on the map, the same as tapping it there.
- **Drag a zone to where you want it in the table** by its ⇅ handle — mouse or finger. The order is remembered on every browser and phone and does not change the order the mower mows in.
- **On a phone the grid turns sideways** with the setting names pinned; the zones scroll inside the table, never the page. **In Fleet Mode** each mower gets its own table, in your mower order.
- **The Mower settings column steps aside while the table shows** (its four settings are the table's first columns), and the map and the table take the full width. An edit left in that column becomes an unsaved table cell. Back on Form, or with the panel closed, the page is as before.

## Fixed

- **A catch-up (multi-pass) mow should no longer be cut off by Do Not Disturb hours.** When the hours began mid-run, the Toolkit mistook the mower's trip home for the end of a pass, ended its task where it stood and tried to start the next pass inside the hours — the mower sat outside until morning and nothing restarted. Now the mower's own task is left alone, the next pass waits until the hours end, and if the mower has not carried on by itself a few minutes after they end, the Toolkit sends it back out to finish (only while its mow is still unfinished, and never a mower you sent home). The Event log says "Do Not Disturb hours began" instead of "NOT commanded by the Toolkit".

## Languages

The new screens are translated in all 15 languages.

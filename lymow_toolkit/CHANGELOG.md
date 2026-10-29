Lymow Toolkit v2.14.5

Sorting and cut-line previews in the Cutting parameters Table, a Table that works on a phone, and the Lymow One's own zone settings after charging and between zones. It keeps your sign-in, settings, maps, layout and history — just update.


- **Cutting parameters Table** — sort the zones by any setting, and see each zone's cut lines while you change the angle.
- **Table on a phone** — tapping a box should no longer zoom the page; the box stays in view.
- **Lymow One** — each zone's own settings should go back on after Recharge & Resume and between zones.


## New

- **Cutting parameters Table: sort the zones by any setting.** Tap a column's name (on a phone, a setting's name in the pinned column, or the Zone corner) to sort the zones by it; tap again to reverse. Numbers sort as numbers, choices by their name, and a dash goes last. The sorted order is remembered on every browser and phone until you sort again or drag a zone by its ⇅ handle.
- **Cutting parameters Table: each zone's cut lines.** Hover a zone's name with a mouse, or tap it, to see that zone alone with its strips at the angle the table shows (a cross-cut draws both directions; Optimized is an estimate). While you change a zone's Strip angle, Pattern or Cross-cut angle, the picture sits next to the box and redraws with every digit you type — on a phone, in the space above the keypad, never over the box.

## Changed

- **The Table gets the whole width.** While the table shows, Mower settings is hidden (its settings are the table's first columns). During a mow, This mow only stays so you can still change the running mow.

## Fixed

- **Cutting parameters Table on a phone: tapping a box should no longer zoom the page.** The table's boxes had text small enough for Safari to zoom in on them, which could push the box you were typing in out of sight. The box you tap is now moved fully into view inside the table, clear of the pinned setting names, and the table keeps its place after a change instead of jumping back to the first zone.
- **Lymow One: each zone's own settings should go back on after Recharge & Resume and between zones.** The Lymow One's firmware raises its deck for channels (including the trip to and from the dock) and doesn't lower it again. After charging, once the mower stops in the zone it was mowing — and after a channel, once it stops in the mow's next zone — the Toolkit pauses it, lowers the deck all the way, puts back that zone's own cut height, blade speed and mowing speed from the mower's map, and resumes. Zones it only drives through are left alone. The Event log shows each step with 🛞, and says if the mower refused the settings or did not resume. The Lymow One Plus is not affected.

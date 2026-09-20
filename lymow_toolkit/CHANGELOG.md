Lymow Toolkit v1.60.1

Everything below is a change from v1.60.0.


- **"Send to" phones stay selected.** In Settings → Home Assistant → Phone notifications, a phone you tick now stays ticked after Save and after Send test. A Save made before the Toolkit has read the phone list keeps your selection instead of resetting it to every phone, and the Toolkit reads the phone list as soon as notifications start, so the list is there after a restart.
- **Zone notifications follow the mow, not the map.** With overlapping zones, "Reached … and started mowing" is now sent only for a zone the mow selected, when the mower reaches it — not for the zones it drives through on the way, and not again on every turn into the overlap. The Home Assistant Current zone sensor should no longer flip between overlapping zones while mowing, and progress milestones are no longer reset by those flips.


## Phone notifications

In **Settings → Home Assistant → Phone notifications**, the phones under **Send to** now stay ticked after Save
and after Send test — before, the panel repainted the selection it had loaded with, so every new tick looked as
if it had been dropped. The Toolkit reads the phone list as soon as notifications start, so after a restart or
after switching notifications off and on the list is there, and a Save made while the list is still empty keeps
your stored selection instead of resetting it to every phone.

## Zones

The mower never reports which zone it is mowing; the Toolkit works it out from the mower's position against
your map. Where zones overlap, the zone reported is now the one being mowed: the zone the running mow selected
and has not finished, kept while the mower is inside it, instead of whichever polygon happens to contain the
mower. "Reached … and started mowing" is sent only when the mower reaches a zone the mow selected, not for zones
it drives through on the way, and not again on every turn into an overlap. The Home Assistant **Current zone**
sensor should no longer flip between overlapping zones, and the progress milestones are no longer reset by such
a flip.

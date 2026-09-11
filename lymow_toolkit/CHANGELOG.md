Lymow Toolkit v1.57.0

Everything below is a change from v1.56.4.


- New: automatic cut-angle rotation. The new "Adjust cut angle offset" option — on the map, next to Multi-pass — turns the cut angle by an amount you choose after every completed mow, so the mower never lays the same stripes twice. Every zone turns from its own angle, including zones set to Optimized; the event log shows the exact angle used each mow.
- New: a scheduled mow's "Rotate the cut angle each run" can now be set to any amount from 1 to 179 degrees, instead of the old fixed 30.
- Removed "Download all to this PC" (a map downloaded to a PC cannot be restored to a mower) and the "Merge zones — coming soon" placeholder.


## Automatic cut-angle rotation

Mowing the same direction every time wears the grass into the same lines and can leave wheel ruts. The new
**Adjust cut angle offset** option — a checkbox on the map, next to Multi-pass — turns the cut angle by a
set amount after every completed mow, so the finish evens out over time.

Turn it on and pick how many degrees to turn each mow. After that:

- The first mow of a zone cuts at its normal angle — its fixed angle, or, for a zone set to Optimized, the
  direction the Toolkit works out the mower would choose.
- Every mow after turns that many degrees further round, wrapping back around at 180.
- Every zone turns from its own angle. Zones set to Chess Board or Adaptive Zigzag are left alone — those
  patterns choose their own direction and cannot take a fixed angle.
- Change a zone's or the global cut angle and the next mow starts fresh from that new angle.
- A Reset button returns every zone to its starting angle.

The event log names the exact angle each mow ("Cut angle offset → Front Yard: 168° this mow"), so you can
see it change. It runs instead of a Multi-pass catch-up, not alongside it.

## The scheduled-mow angle rotation is adjustable

A scheduled mow could already turn its cut angle a little on alternating runs so a repeating schedule did
not cut the identical pattern twice. That turn was fixed at 30 degrees; you can now set it to any amount
from 1 to 179.

## Removed two controls that could not work

**Download all to this PC** downloaded a mower's maps to your computer, but a map file on a PC cannot be put
back on a mower — there is no way to restore one — so the download served no purpose. It has been removed.
To back up and restore a map, use the restore points, which save to and restore from the cloud.

The **Merge zones — coming soon** placeholder has also been removed. Merging existing zones into one works
in the official app but needs Bluetooth, which the Toolkit cannot do, so it was never going to arrive.

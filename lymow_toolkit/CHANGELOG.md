Lymow Toolkit v1.58.0

Everything below is a change from v1.57.0.


- New: Plot on Error. Pick the error or warning codes you care about and the mower marks exactly where on your map it hit one — a colored, tappable marker with the code, plus a line in the event log with the latitude and longitude. When there is no live satellite position (often the moment it stops), the marker uses the last known spot and is flagged approximate.
- The map's overlay switches — Mowed, Precision heat, Link heat and Freshness — now sit on one row, directly under the map controls, so they are easier to reach.


## Mark faults on the map

When the mower stops on a fault, the hardest part can be finding where it happened. The new **Plot on
Error** switch — on the map, in the overlay row — solves that.

Open its ⚙️ and:

- Pick a color for the markers.
- Add the error or warning codes you want to see, from a drop-down of the codes the mower actually reports
  (for example E44 — Bumper jammed). Press ＋ to add another, ✕ to remove one. The list is sorted with the
  error (E) codes first and the warning (W) codes after, each in numeric order, so a code is easy to find.
- Save.

From then on, every time the mower reports one of those codes a colored marker drops on the map at that
spot. Tap a marker to see the code, the time, and the exact position. If the mower has no live satellite
position at that moment — often the case the instant it stops — the marker uses its last known position and
is flagged approximate.

Every marked fault is also written to the event log with its latitude and longitude, so the trouble spots in
your yard are easy to track down. Only faults that happen after you switch it on are shown.

## The overlay switches are on one row

The map's overlay switches — **Mowed**, **Precision heat**, **Link heat** and **Freshness** — now sit on a
single row, directly under the Satellite / Street map / map controls, instead of stacked off to the side.
They are easier to find and reach.

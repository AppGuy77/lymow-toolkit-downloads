Lymow Toolkit v1.51.1

Everything below is a change from v1.51.0.


- Zone previews now show what the next mow will actually cut — never settings lingering on the mower, and never a stale flash before the truth loads.
- The Mow pattern box always tells the truth: a mower still storing Chess Board (cross-cut) from an old setup now shows it, so you can switch it off with one Save.
- Updates and reinstalls always install cleanly (no more silent Windows "repair" mode breaking the service). Add/Remove Programs now shows a technical number like 1.51.199 — normal; the real version is in the app.


## Previews that match reality

Zone thumbnails used to render settings as stored ON THE MOWER — which can include a cross-cut
pattern you turned off in the Toolkit long ago (the mower keeps old settings until something
rewrites them). Zones then previewed crossed stripes nobody had selected. Previews now layer your
Toolkit settings over the mower's stored ones exactly the way a mow start applies them, so what
you see is what the next mow cuts. And a preview never paints a stale pattern first: it waits for
the truth and paints once, right.

## The pattern box tells the truth

If your mower still stores Chess Board (cross-cut) globally from an old setup, the Cutting
parameters pattern box now SHOWS "Chess Board (cross-cut)" instead of silently displaying
"Zigzag." To clear a leftover cross-cut: deselect all zones, open Cutting parameters, pick
Zigzag, Save — done permanently. The pattern box and the Cross-cut checkbox are now one setting
shown two ways, always in agreement, and an incomplete Chess Board setup can no longer be saved.

## Clean installs, always

Installing a Toolkit build over the same version could silently enter Windows "repair" mode
instead of installing, which could break the service until an uninstall/reinstall. Installer
versions now strictly ascend so every install is a true install. Side effect: "Add or remove
programs" shows a technical version like 1.51.199 — that is expected; the human version is in
the app header and the installer file name.

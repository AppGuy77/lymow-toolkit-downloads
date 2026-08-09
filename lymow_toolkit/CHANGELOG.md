Lymow Toolkit v1.47.0

Everything below is a change from v1.46.3.


- The crossing sweep of a cross-cut is now painted in its own color, so you can see whether it missed anything.
- Pick that color and how see-through it is, right beside the Cross-cut checkbox.
- Both colors stay on the map after the mow, and a new mow now clears only the zones it will actually cut.
- The map remembers where you panned and zoomed to, with a new button to put the whole yard back.


## New

**See what the crossing sweep actually covered.** A cross-cut mows the same zone twice, in two
directions, and both used to be painted the same green — so there was no way to tell whether the
second sweep had missed a strip. The crossing sweep is now painted in its own color (orange by
default) on top of the first, so anywhere it has not reached yet still shows as mowed underneath and
stands out.

**Choose the color and its transparency.** Both sit next to the Cross-cut checkbox — in Cutting
parameters and in the multi-pass panel. It is one setting, so changing it in either place changes it
in the other. Turn the transparency down to see the first sweep through the second and compare them.

**The map remembers where you left it.** Your pan and zoom are kept for each mower instead of
snapping back to the whole yard every time you open the Toolkit. The new 🔄️ button beside the
fullscreen button puts the whole yard back.

**A wiki link in the header**, beside the version number, opening the full user guide in a new tab.

## Changed

**A new mow clears the paint only for the zones it will cut.** Previously, starting any mow cleared
the whole map for that mower. Mow the front and the back stays exactly as you left it. The 🗑️
button still clears everything for that mower whenever you want a clean slate.

**Finished zones keep their colors.** Both the first sweep and the crossing sweep stay on the map
through a completed mow, a cancelled one, and a return to the dock.

## Worth knowing

**Mows started from the official Lymow app.** When a mow is started from the official app — or by a
schedule set inside it — the mower never tells the Toolkit which zones that mow will cover. It only
reports zones as it finishes them. Mows started from the Toolkit are unaffected. The practical
effect: if an app-started mow is cancelled part-way, the Toolkit cannot tell which zone that partial
paint belongs to, so it is cleared when the next mow starts rather than kept. Zones that finish are
recorded correctly either way.

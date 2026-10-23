Lymow Toolkit v2.13.1

Change the mow that is running, and map editing that reports the mower's decision. It keeps your sign-in, settings, maps, layout and history — just update.


- **Change the mow that is running** — a This mow only panel in Mower settings: cut height, mowing speed, blade speed for the current mow; applying while cutting pauses, changes, resumes.
- **Map editing by driving says what the mower decided** — Done reports saved or refused, with the mower's reason; a refused shape stays open to drive on.
- **A boundary edit is two steps** — drive onto the existing boundary, press Start, redraw, press Done.


## New

- **Change the mow that is running.** Mower settings shows a **This mow only** panel while a mow is in progress: cut height, mowing speed and blade speed for the current mow, every zone in it. Your saved zone settings are not touched. Apply while the mower is cutting and it pauses, makes the change, and resumes; apply while it is paused and it stays paused for you to resume when you are ready. The panel says whether the mower accepted or refused the change.

## Fixed

- **Map editing by driving now reports what the mower decided.** Start waits for the mower to accept the recording. Done says whether the mower saved the shape or refused it, in the Lymow app's own words — for example "this change would make the connected channel invalid" — and a refused shape stays open so you can drive on and press Done again, or Cancel. Before, the Toolkit said Saved whatever the mower did.
- **A boundary edit is two steps.** Pick the zone, drive the mower onto the existing boundary, press Start, redraw the edge, finish on the old boundary, press Done. The mower measures the start and the end of your drive against the old boundary, so Start no longer fires the moment you pick the zone.
- **A docking channel the mower saves itself should now close the recording.** The mower saves a channel that leads to the dock when it reaches and reads the dock; the Toolkit now notices and clears the banner instead of waiting for a Done that is already done.
- **Remote control no longer sends a Pause while the mower is recording a map shape** (the "did not follow a command: Pause" lines).
- **Edit Map stays usable while a recording is open**, and a reload picks the recording back up.
- **Phone held sideways:** the camera's ✏️ Edit Map button is no longer hidden under the overlay toggles in fullscreen.

## Languages

The new panel and the new messages are translated in all 15 languages.

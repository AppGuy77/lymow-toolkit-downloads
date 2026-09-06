Lymow Toolkit v1.56.1

Everything below is a change from v1.56.0.


- Fixed: the satellite photo alignment now follows you to every browser, phone and mower in the same yard — it is saved for the yard and the imagery source, not for one mower or one browser
- Fixed: the header names the real connection state ("no mower selected", "connecting…", "could not connect: reason", "could not reconnect after restart: reason") instead of "offline", and a new browser opens on the same mower as every other
- Fixed: every setting follows you to every browser — map look, overlays, remote-control and camera choices, calendar view, mow order and multi-pass passes are saved on the Toolkit


## The satellite photo alignment follows you

Lock the photo once and every browser, phone and mower in the same yard shows the same aligned
picture. The alignment is saved on the Toolkit for the **yard and the imagery source** (Esri, Google,
your own URL), not for one mower or one browser. A second mower in the same yard shares it without
being aligned again; a mower somewhere else keeps its own. Alignments you already locked are carried
over the first time each mower's map is drawn. The away link's mini-map draws the aligned photo too,
and the unlocked photo can be dragged on a phone. **Lock** only says "locked" once the alignment
really reached the Toolkit; if it did not, the photo stays unlocked and the message says why.

## The header says what is actually going on

One word, "offline", used to cover four different situations. The header now says **"no mower selected
— pick one above"**, **"connecting…"**, **"could not connect: (reason)"** or **"could not reconnect after
restart: (reason)"**, and the reason is written to the Toolkit's log. A browser that has never opened
on your Toolkit (a phone, the away link, a second computer) opens on the same mower as every other
browser instead of waiting on the mower list. With one mower nothing changes: it is picked for you as
before.

## Every setting follows you

These were kept in the browser that set them and are now saved on the Toolkit, so they are the same
in every browser and on every phone: satellite, street map, imagery source and custom URL; the mowed
area, freshness, precision and link overlays; the remote's drive speed, joystick size and remembered
cut height; the camera's keep-alive and pinned controls; the calendar view; the open Settings section;
the mow order and the multi-pass passes (both per mower). Map choices you made in one browser before
v1.54.2 are handed to the Toolkit the next time that browser opens, so the other browsers pick them up.

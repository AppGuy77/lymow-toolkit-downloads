Lymow Toolkit v2.14.4

A Lymow One deck reset at the spot where the mow resumes, and the Edit Map button back on the phone's Remote. It keeps your sign-in, settings, maps, layout and history — just update.


- **Lymow One** — the deck reset should now happen where the mow resumes: the spot where it stopped mowing after Recharge & Resume, and the next zone after a channel.
- **Remote control on a phone** — ✏️ Edit Map is back with two joysticks, next to ✕ Exit in fullscreen.


## Fixed

- **Lymow One: the deck reset should now happen where the mow resumes.** The Lymow One's firmware raises its deck for channels (including the trip to and from the dock) and doesn't lower it again, so it kept cutting at the channel height. When a Lymow One with its mow open heads home to charge, the Toolkit now records the exact spot where it stopped mowing. When the mower is back at that spot, it pauses, sends the deck all the way down (the same as the Remote's Deck control at its lowest), waits for the deck and resumes. After a channel crossing into the mow's next zone it does the same as soon as the mower is in that zone. Zones it only drives through are left alone. The Event log shows each reset as **🛞 Lymow One deck reset**, and says if the mow ended before the mower got back to that spot. The Lymow One Plus is not affected.
- **Remote control on a phone: ✏️ Edit Map with two joysticks.** With two joysticks the Edit Map button was hidden, and in fullscreen on a phone there was no other way to start editing the map. In fullscreen it now sits next to ✕ Exit, with one joystick or two.

## Languages

The new messages are translated in all 15 languages.

Lymow Toolkit v2.12.2

A game-controller fix. It keeps your sign-in, settings, maps, layout and history — just update.


- **The game controller you press is the one the Remote reads** — a Bluetooth headset that shows up as a "controller" no longer takes over.


## Fixed

- **The game controller is the one you press, not the first device your computer lists.** Some Bluetooth headsets show up to the browser as a game controller, and the Remote used to read whichever device was listed first — so an Xbox pad could be "identified" as the headset, and restarting did not help. **Set up controller** now waits for you to press a button on the controller you want and remembers that controller for this kind of device (phone, tablet or computer); from then on it is the only one the Remote reads. Hover **Connected** or **None** on the Remote tab to see which controller the Toolkit is listening to. If the remembered controller is off, the Remote shows None even while the headset is on.

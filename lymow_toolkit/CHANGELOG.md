Lymow Toolkit v1.48.1

Everything below is a change from v1.47.1.


- New: Return to dock path — Direct Route or Follow Perimeter — in Settings → Mowing options.
- Fixed: Mow in rain "Off" and the Charging Handbrake never actually applied. Nor would Follow Perimeter have.
- "Charging lock" is now "Charging Handbrake", set to On or Off, and the dropdowns no longer say "Select…".
- Fixed: in the fullscreen map the ✕ Exit button covered the camera button, and reset view was missing.


## New

**Return to dock path.** The same setting the official app has, now in **Settings → Mowing
options**: **Direct Route** sends the mower straight back across the lawn, **Follow Perimeter** takes
it round the zone edge instead. It is stored on the mower, so it applies to every trip home including
scheduled mows and mows started from the app.

The Toolkit has always respected whatever you had set in the app — it never overwrote it. There was
simply no way to change it from here.

## Fixed

**Settings whose value is "zero" never reached the mower.** This affects controls you already had:
**Mow in rain → Off** and the **Charging Handbrake**, plus the new **Follow Perimeter**. All three
are sent as a value of zero, and zero was being dropped from the message on the way out. The mower
does not treat a missing value as "set it to zero" — it keeps what it already had. So choosing those
options appeared to work and changed nothing. They are sent properly now, and the Toolkit reads the
setting back off the mower afterwards rather than assuming.

**The message these settings travel in now matches the official app exactly.** It carried two extra
pieces of information the app does not send, which can cause the mower to ignore a settings write.

**Charging Handbrake.** "Charging lock" is renamed to what it actually is — a parking brake that
locks the mower's wheels while it is charging so it cannot roll or be pushed off the dock contacts —
and it is simply **On** or **Off**.

**The Mowing options dropdowns no longer say "Select…".** Each shows what your mower is actually set
to. Until the mower has reported a setting the control waits instead of displaying a value it has not
confirmed.

**Fullscreen map buttons.** The **✕ Exit** button was drawn directly on top of the **camera** button,
and the **reset view** button was hidden in fullscreen altogether. Every corner button now stacks
properly and stays reachable.

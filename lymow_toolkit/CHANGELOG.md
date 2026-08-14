Lymow Toolkit v1.49.1

Everything below is a change from v1.49.0. Three fixes, no new features.


- Fixed: the map could draw a backup you saved months ago as though it were your mower's current map.
- Fixed: a mower parked on its dock could show no mower icon on its own map.
- Fixed: "Stay signed in" could forget your password by itself and send you back to the sign-in screen.
- When the mower's map isn't available, the Toolkit now says why instead of just "waiting".


## Fixed

**The map could show you an old map and say nothing.** When your mower's own map had not arrived
yet, the Toolkit worked down a chain of fallbacks — and the last one was a **backup you had saved**,
possibly months earlier. It was drawn like any other map: no date, no marking, no way to tell it
apart from the real thing. Once zones have been edited, or a different map made active, that file is
simply wrong.

Backups exist so a map can be **restored**, not so one can be displayed. They are no longer drawn at
all, and restoring them is completely unchanged.

There was a second way to see an old map: the Toolkit remembers the last good map it received, so a
briefly corrupted update doesn't blank the screen mid-mow. That memory had no time limit, so if the
mower stopped reporting entirely, the remembered map stayed on screen looking current. It now only
applies while the mower is actually sending data.

And when there is no map to show, the Toolkit says **why**: the mower is asleep, another app is
holding your account's single cloud connection, it is reconnecting, or your sign-in expired. When it
shows the copy from your Lymow account, it tells you how old that copy is. Previously it said only
that it was waiting, which made a five-second wait look identical to a mower that had been asleep
since Tuesday.

**A mower could be missing from its own map.** If it was parked at the map's origin point, the
Toolkit drew no mower icon at all — while a second mower out on the lawn appeared normally. The
mower's position was being read from one source that reports nothing in that exact situation.

It now reads from every source available, so the icon appears whenever anything knows where the
mower is. When genuinely nothing does — some mowers only report a position while mowing — the map
says so instead of quietly leaving the mower off.

**"Stay signed in" could forget your password.** Roughly one saved password in thirty was
unreadable the next time the Toolkit needed it, so you were sent back to the sign-in screen with no
explanation, as if you had never ticked the box. This was a fault in how the saved password was
locked to your machine, and it affected v1.49.0 only.

If it happened to you: sign in, tick **Stay signed in** once more, and it will stay this time.
Nothing was exposed — the failure was that the password could not be read back, not that anyone
else could read it.

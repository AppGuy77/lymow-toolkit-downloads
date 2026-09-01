Lymow Toolkit v1.53.1

Everything below is a change from v1.53.0.


- Remote control no longer gets stuck if the camera drops. If the live camera dropped while you were driving the mower by hand and couldn't reconnect, the mower could be left unable to resume — it now steps out of remote control and pauses the mow, so Resume, Dock and Cancel all work again.


## Remote control recovers when the camera drops

Driving the mower by hand puts it into remote control. If the live camera dropped in that state and
couldn't reconnect, the mower stayed locked in remote control, where it quietly ignores Resume — so
the mow was stuck and pressing Resume (or the "Resume mowing" override) did nothing.

Now, when the camera is lost and can't come back, the Toolkit steps the mower out of remote control
and leaves the mow **paused** (it never cancels it), and tells you it did. From there **Resume** works
normally. The same applies if the mower was left in remote control for any other reason: **Resume**,
**Dock** and **Cancel** all take effect instead of being ignored.

If the whole connection to the mower dropped — not just the camera picture — no button can reach it
until the link comes back; this covers the common case where the camera stream stops but the mower is
otherwise still connected.

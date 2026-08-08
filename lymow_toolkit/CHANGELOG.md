Lymow Toolkit v1.46.2

A fix release. Everything below is a change from v1.46.1.


- The mower is only sent back out after charging if "Enable auto-recharge & resume" is on, at your resume level.
- Sending the mower to the dock keeps it there — it stays put until you resume it.
- Charging lock and Mow in rain show what the mower is set to instead of "Select…".
- Your last saved map shows straight away instead of a blank map area.
- The map recovers on its own after a restart instead of sitting on "Loading…".
- Weak RTK signal (#15) recovery waits for the signal instead of retrying into it.
- Selected zones and their mow order come back when you reopen the app.
- Windows: the size in Add or remove programs is correct.
- Updates no longer leave the installer behind (about 143 MB per machine).


## Fixed

**The toolkit no longer sends the mower back out after charging unless you have asked it to.** The
only thing that decides this is "Enable auto-recharge & resume" on your mower, under Settings →
Auto-recharge. With it switched off, the toolkit was sending the mower out anyway; with it on, it
waited for 80% no matter what "Resume after charging to" level you had set. Both now come from the
mower.

**Sending the mower to the dock keeps it there.** After you docked it, the toolkit could send it back
out again once it had charged, even though you had just brought it in. It stays docked until you
resume it or start a new mow.

**Charging lock and Mow in rain show what the mower is set to.** Both read "Select…" whatever the
mower's real setting was. They now show the current value, and a change is checked against the mower
before it is reported as saved.

**Your last saved map shows while the mower's current map loads.** The map area stayed blank — no
zones, no satellite image — until the current map had streamed in, which can take the better part of
a minute. Map changes stay locked until the mower's own map arrives.

**The map recovers on its own after a restart.** It could stay on "Loading this mower's current map…"
indefinitely, most often after an update, until the official app was opened.

**Weak RTK signal (#15) recovery waits for the signal to come back.** Clearing that fault while the
signal was still weak only raised it again, and after three attempts the toolkit gave up. It now
waits for a steady fix first, and attempts held back while waiting do not count against the limit.

**Selected zones come back when you reopen the app.** The zones picked for a mow, and their mow
order, were lost when the app was closed. They are restored while the mow is running.

**Windows: the size in Add or remove programs is correct.** It was reported far higher than what is
actually installed.

**Updates no longer leave the installer behind.** Every updated machine kept the installer it last
used — about 143 MB — along with its installation log. Both are removed once the update has landed,
and anything already left behind is cleaned up. The mower monitoring log is capped as well, so it can
no longer grow without limit.

## Updating

Update from inside the Toolkit (the ⚠️ beside the 📖), or download below.
Docker/Unraid: pull the image again. Home Assistant: Update on the add-on page.

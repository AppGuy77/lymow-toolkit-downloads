Lymow Toolkit v1.48.2

Everything below is a change from v1.48.1.


- Fixed: a mower could show as "(offline)" in the mower list while its live data was on screen.
- Fixed: finishing a zone painted the whole zone green, including ground the mower never reached.
- Fixed: "Update check failed — certificate verify failed" on machines that were otherwise fine.
- RTK logs now record about every 2 seconds instead of every 30, so they show your mower's real reporting rate.


## Fixed

**A mower could show as "(offline)" while it was running.** The word beside your mower's name in the
mower list was read once, when the Toolkit started up, and then never checked again. If your mower
happened to be asleep at that moment — on the dock overnight, powered off, or off the network — it
stayed labeled offline for as long as the Toolkit kept running, even with its live data on the screen
in front of you. Nothing was wrong with the mower.

That word is now re-checked as you use the Toolkit, and while you are connected to a mower it comes
from that mower's own live data rather than a stored answer. If the state cannot be confirmed at that
moment, the name is shown on its own — better to say nothing than to show a word we cannot stand
behind.

**Finishing a zone painted the whole zone green.** When a zone completed, the map filled its entire
shape in, on the reasoning that a finished zone should not look patchy. But that covered ground the
mower never actually reached: around obstacles, strips it skipped, corners it could not get into. The
map showed a clean finished lawn whether or not the mower had cut it.

The map now shows only what your mower reported cutting. A finished zone can therefore show real
gaps — that is the point, and it is worth knowing that a zone will look less uniformly green than it
did before. This applies to ordinary mows and cross-cut mows alike.

**"Update check failed — certificate verify failed."** On some machines the Toolkit could sign in,
show your mower and run perfectly, yet fail to check for or install updates with a certificate error.
It looked like an antivirus or network problem, and the Toolkit's own message unhelpfully suggested
exactly that. It was neither. Different parts of the Toolkit were checking internet certificates
against different lists, and the part that handles updates was using one that is empty on some
installs.

Every internet connection the Toolkit makes now uses the same verified list of certificates, added to
whatever your own computer already trusts, so nothing that worked before stops working. If a check
does fail, the message now says what was actually verified instead of guessing.

If your workplace or antivirus genuinely does inspect secure connections, you can point the Toolkit
at its certificate by setting `LYMOW_CA_BUNDLE` to that file.

## Improved

**RTK logs record about every 2 seconds instead of every 30.** With recording switched on, the
Toolkit now asks your mower for satellite and radio readings as fast as the mower is willing to
answer. Before, with no browser open, it only asked every 30 seconds — so the log showed how often
*we* were asking rather than how often your *mower* was reporting, and a mower reporting quickly
looked identical to one reporting slowly.

Recording uses noticeably more data while it is switched on, so turn it off when you have finished
capturing.

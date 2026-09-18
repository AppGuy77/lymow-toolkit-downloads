Lymow Toolkit v1.59.4

Everything below is a change from v1.59.3.


- **"Address in use by another Toolkit" with only one Toolkit — fixed.** After an update, the away link opened by the previous version could stay running on the computer and keep your mower-xxxx address, so the new version was refused its own address and blamed a second Toolkit that did not exist, while the address itself kept working. The Toolkit now closes its away link before restarting for an update, takes the address back from any leftover copy on the same computer, and the relay hands an address to a newer connection from the same Toolkit.


## "Address in use by another Toolkit" with only one Toolkit

The Toolkit restarts for an update with a hard exit, which skipped the step that closes the away link.
On computers whose service manager leaves child processes running (macOS, and any Toolkit started by hand),
the previous version's link kept running, kept holding your mower-xxxx address at the relay, and kept
forwarding it into the new version's port. The address worked; the new version's own link was refused
every time, and the mark beside the Away access switch read **Address in use by another Toolkit on this
account** with only one Toolkit installed.

This release fixes it in three places:

- **The Toolkit closes its away link before every restart** — for an update, for the Shut down button and
  for the automatic restart after a version change.
- **The Toolkit takes its address back.** At start, and whenever the relay reports the address as held,
  it looks for a leftover link of this same install on this computer and closes it, and it checks who is
  actually answering at the address before it says anything.
- **The relay hands an address to a newer connection from the same Toolkit.** A connection with the same
  device key that already holds the address replaces the older session. A different Toolkit on the same
  account is still refused, which is the only case that is really "another Toolkit".

The mark beside the Away access switch now tells the three cases apart: **Address in use by another
Toolkit on this account** only when a second Toolkit actually answered at your address; **Taking the
address back from an old copy of this Toolkit** for a few seconds while a leftover is being reclaimed; and
**The relay refused this address — re-registering** when nobody is behind the address and the relay does
not yet know this Toolkit's key for it, which re-registers by itself.

Update from inside the Toolkit, or from the downloads page. Home Assistant: Update on the add-on page.
Docker: pull the image again.

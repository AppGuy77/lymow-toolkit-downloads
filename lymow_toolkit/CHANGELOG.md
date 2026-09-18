Lymow Toolkit v1.59.1

Everything below is a change from v1.59.0.


- **The Away access status should no longer flicker between "Starting" and "Service not running".** Two Toolkits on one Lymow account (for example a Home Assistant add-on and a PC) no longer knock each other off the relay every 30 seconds, and the mark beside the switch now names the real cause: **Key rejected by the relay — re-registering**, **Address in use by another Toolkit on this account** or **Relay unreachable**.


## The Away access status stops flickering

If you saw the mark beside the **Away access** switch alternate between ⌛ Starting and ❌ Service not
running every few seconds while your mower-xxxx address still opened on your phone, this is the fix.

The cause was on the relay: it kept only one key per Lymow account, so when two Toolkits were signed in
to the same account — for example a Home Assistant add-on and a PC, or a new PC while the old one was
still running — each new registration threw the other Toolkit off. The thrown-off one re-registered about
30 seconds later and threw the first one off in turn, for as long as both ran. Your address kept working
from whichever Toolkit held it at that moment, which is why the phone was fine while the switch flickered.

The relay now keeps every device's key, so both Toolkits stay registered. Only one of them can hold your
address at a time, and the Toolkit now says so instead of flickering. The mark beside the switch is one of:

- ✅ — the away link is up.
- ⌛ **Starting** — the link is connecting.
- ❌ **Key rejected by the relay — re-registering** — heals itself within about 30 seconds.
- ❌ **Address in use by another Toolkit on this account** — a second Toolkit signed in to the same Lymow
  account already holds your address. Only one can at a time; this one checks again every 30 seconds and
  takes over when the other one goes away.
- ❌ **Relay unreachable** — this computer cannot reach the relay server right now.
- ❌ **Service not running** — away access is off, or its helper is not running on this computer.

Hover the **?** beside the switch for the same list, and the glossary (📖) has an **Away access status**
entry. A Toolkit that is refused now also waits longer between retries instead of knocking every few
seconds, and its log says why a re-registration did not work when it does not.

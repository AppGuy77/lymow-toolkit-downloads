Lymow Toolkit v1.50.0

Everything below is a change from v1.49.1.


- New: the Toolkit runs inside Home Assistant — a sidebar panel, with every mower on your account published for automations.
- New: keep your stripes — an optional setting so canceling a mow no longer turns the zones it already cut red.
- New: resume a mow that has already started for the dock, from the "Mow on hold" card.
- Fixed: with more than one mower, switching to another could leave it stuck on "Connected — idle"; it now goes live with its own map.
- Fixed: the sign-in screen's phone QR — centered, a real away-from-home link (not just your local address), and Save-to-Home only for your permanent link.
- Fixed: logging out could leave you signed in, and an in-app update on Windows could fail.


## Home Assistant users — please read before updating

This release adds the Toolkit as a **Home Assistant sidebar panel** (ingress). Because that changes
how the add-on is wired into Home Assistant, the first setup after updating can need a little
patience:

- **You may need to run "Clear Data" and "Set up Home Assistant" more than once** until everything
  repairs cleanly. If the panel or the mower entities look wrong after the update, open the Toolkit's
  Home Assistant setup, **Clear Data**, then **Set up Home Assistant** again — repeat until it comes
  up clean. This is a one-time settling after the change, not a fault with your mower.
- **The automations integration needs a long-lived access token.** To let Home Assistant automations
  control your mowers, create a **Long-Lived Access Token** in Home Assistant (your profile →
  Security → Long-Lived Access Tokens) and give it to the Toolkit's Home Assistant setup when asked.
- **On a low-powered Home Assistant system** (an older Raspberry Pi or a small VM), **signing in with
  Google can be slow or difficult** — the sign-in runs a browser on the box, and limited memory or a
  slow disk can make it struggle. A computer, a Mac, or a faster machine handles it easily, or sign
  in with your **email and password** on the Home Assistant box instead.

## New

**The Toolkit runs inside Home Assistant.** It installs as a **sidebar panel**, opened from Home
Assistant itself with Home Assistant's own login, and it works through Nabu Casa remote access.
**Every mower on your account is published to Home Assistant**, so your automations can see and
control any mower — not only the one you happen to be looking at.

**Keep your stripes when you cancel a mow.** Off by default. Turn it on in the Freshness settings and
canceling a mow **keeps the zones it already finished marked as freshly mowed**, instead of turning
them red. It's for the workaround where you cancel to stop the mower driving across finished stripes
to reach the rest, hand-mow the awkward bits, and restart elsewhere. Only the zones actually finished
before you cancel are kept — never the one it was mid-way through.

**Resume a mow that has started for the dock.** A **Resume mowing** button on the "Mow on hold" card
sends the mower back out to finish, even when it has already turned for home.

## Fixed

**Switching between mowers could leave one stuck on "Connected — idle".** With more than one mower,
selecting a different one could leave it connected but never going live, showing an old map.
Selecting a mower now brings **it** live and draws **its own** map straight away.

**The sign-in screen's phone QR code.** It was left-justified — now **centered**. It only ever showed
your **local network address**, so it was no use for logging in from your phone or from away — now it
gives you a **working away-from-home link**. And it used to invite you to **Save it to your Home
Screen even when the link was temporary** and would stop working after a reboot — Save-to-Home is now
only offered for your **permanent** link.

**Logging out.** Logging out could fail and leave you signed in. It now logs you out.

**Updating from inside the app.** On Windows, an update applied from within the Toolkit could fail.
In-app updates now complete cleanly.

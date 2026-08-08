Lymow Toolkit v1.46.3

A fix release for Linux and macOS. Everything below is a change from v1.46.2.


- Linux and macOS: the away-from-home link and its QR code now appear, instead of only your home-WiFi address.
- The Toolkit installs the away-access helper itself and checks that it works before using it.
- The phone screen now says when that helper is downloading, or why away access cannot start.


## Fixed

**Linux and macOS: the away-from-home link and its QR code now appear.** On those two systems the
away link needs a small helper program (cloudflared), which is downloaded while the Toolkit installs.
If that download did not finish — a slow moment on the network, a proxy, a firewall — away access
could never start, and nothing anywhere said so: the phone/QR screen simply showed your home-WiFi
address as though nothing else had been asked for.

Three things changed:

- **The Toolkit installs the helper itself.** It checks at every start, and again whenever you switch
  away access back on, so this is now a retry rather than a reinstall. It only ever does this while
  away access is switched on.
- **The helper is checked before it is used.** An unfinished download left a file that looked
  installed but could not run. Nothing is used now until it has actually started and reported its
  version, on the Toolkit and in the installer alike.
- **The phone screen tells you what is happening** — that the helper is downloading, or the reason
  away access cannot start — and still shows your home-WiFi link and QR meanwhile.

Windows, Docker and Home Assistant already included the helper and are unchanged by this release.

If you are on Linux or macOS and the away link never appeared, updating to this version is all that
is needed; there is nothing to install by hand. The installer also writes what it did to
`vendor/cloudflared/install.log`.

# Security Policy

The Lymow Toolkit controls **real hardware with spinning blades**, so we take
security and responsible disclosure seriously. This document is both our
**security policy** and our **vulnerability disclosure policy**.

## Supported versions

We support the **latest release** only. Please update before reporting.

| Version            | Supported |
| ------------------ | --------- |
| Latest (v1.34.x)   | ✅        |
| Anything older     | ❌        |

## Reporting a vulnerability

**Please report privately.** Do **not** open a public issue for a security
problem, and do **not** post working exploits in the community group.

Use GitHub's **private vulnerability reporting**:

1. Open the **Security** tab of this repository → **Report a vulnerability**, or
   go directly to
   **https://github.com/AppGuy77/lymow-toolkit-downloads/security/advisories/new**
2. Describe the issue, its impact, and how to reproduce it.

That opens a private advisory only the maintainer can see. If you can't use it,
open a normal issue that says only *"security — please make contact"* with **no
details**, and we'll arrange a private channel.

### What to include

- What the vulnerability is and its impact.
- Steps or a proof-of-concept to reproduce it.
- The affected version and platform.
- **Do not include** your Lymow account credentials, tokens, or your map / GPS /
  coverage data.

### Our commitment (coordinated disclosure)

- We'll acknowledge your report within **7 days**.
- We'll work on a fix and keep you posted on progress.
- We'll credit you (if you'd like) when the fix ships.
- Please give us reasonable time to fix the issue before disclosing it publicly.

### Safe harbor

We consider good-faith security research that follows this policy to be
**authorized**, and we won't pursue action against researchers who act in good
faith, avoid privacy violations and service disruption, only interact with their
**own** devices and accounts, and give us a chance to fix issues before
disclosure.

## Scope

**In scope**

- The Toolkit's local dashboard web server and its API.
- The authentication / access gate.
- The optional remote-access (Cloudflare tunnel) configuration.
- The device-control command paths and their safety gates.

**Out of scope**

- The Lymow cloud service and the (reverse-engineered) device protocol itself.
- Anything that requires the attacker to already have your Lymow account login.
- Running with a weak dashboard password **and** the remote tunnel enabled — that
  is a configuration choice, not a vulnerability.
- The official Lymow app, cloud, or mower firmware — report those to **Lymow**.

## Running the Toolkit securely (operator guidance)

- The dashboard is a **password-protected local web server** — choose a strong
  password.
- **Remote access (the Cloudflare tunnel) is off by default.** Only enable it if
  you accept that it exposes the dashboard to the internet (still behind your
  password). LAN or a VPN is safer.
- It signs in with **your own** Lymow account. Never share credentials, and never
  commit them anywhere.
- **Physical safety:** never rely on remote start/stop or the software safety
  guards as a substitute for keeping people, pets, and hands away from the blades.

## About this project

Independent community project, **not affiliated with Lymow**, provided "as is"
with no warranty (see the license). Vulnerabilities in the official Lymow app,
cloud, or mower firmware should go to Lymow, not here.

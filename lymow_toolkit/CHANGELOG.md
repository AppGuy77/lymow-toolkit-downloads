Lymow Toolkit v1.51.0

Everything below is a change from v1.50.3.


- New: Two-Factor Authentication for the Toolkit sign-in — password + a 6-digit code from any authenticator app. Enable it in Settings → Security, or right on the Create-a-password screen on a fresh install.
- "Remember this device for 30 days" skips the code on your own devices; recovery codes cover a lost phone; Settings can sign every remembered device out at once.
- The live camera now works away from home on iPhone and Android through your away link — fetched through the Toolkit, mower on WiFi, no cellular data.
- Every camera failure now says why, on screen and in the event log.
- Home Assistant: fixed a freeze right after startup.


## Two-Factor Authentication

Optional, off by default, and it protects the Toolkit's own sign-in — your Lymow account login is
unchanged. With it on, unlocking the dashboard takes your app password plus a 6-digit code from an
authenticator app. Any standard app works: Google Authenticator, Authy, 1Password, the iPhone's
built-in authenticator.

**Already running the Toolkit:** Settings → Security → **Enable Two-Factor Authentication**. Scan
the QR with your authenticator (or type the setup key), enter one code to prove the app works —
two-factor only turns on after that proof, so you can never lock yourself out — then save the
8 one-time recovery codes it hands you.

**Setting up fresh:** the **Create an app password** screen has an **Enable Two-Factor
Authentication** switch. Flip it, set your password, and the same QR setup runs before you ever
see the dashboard.

**Day to day:** tick **Remember this device for 30 days** at sign-in on your own devices and the
code is skipped there. Lost the phone? Each recovery code signs you in once. Settings can mint a
fresh set of recovery codes, and **Forget remembered devices** signs every remembered browser out
at once. If you are ever fully locked out, the existing password reset still works — it clears
two-factor along with the password, and (as always) also signs the Toolkit out of your Lymow
account, so a reset alone never exposes the mower.

Home Assistant users who open the Toolkit inside HA are not asked for a code — Home Assistant
already signed you in.

## The camera, away from home

Through your away link the live picture is now fetched **through the Toolkit** — the server sits
on the mower's network and relays the video out over the same secure link the dashboard uses. That
means it works from anywhere on iPhone and Android, with the mower on WiFi and **no cellular
data**. At home nothing changes: you keep the direct, lowest-latency picture. iPhone plays the
remote picture through Apple's own video pipeline, which runs a few seconds behind live — that is
how iPhone streaming works everywhere, not a defect. If a camera ever fails to start, the screen
now says the actual reason, and the event log records one line per attempt.

## Home Assistant startup freeze

On the first page load after a restart, the server could hang for a few seconds while reading a
system file on slow storage — reported from a community install's watchdog. The read now happens
in the background at startup, before any page can pay for it.

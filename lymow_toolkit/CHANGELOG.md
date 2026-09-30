Lymow Toolkit v2.8.4

An update for everyone on v2.8.3. It keeps your sign-in, settings, maps and history — just update.


- **Every language should be as fast as English** — the page should respond as quickly as in English and open already in your language.
- **Keep camera on for remote control** — the camera and the session keep going when the window is not in front; only Stop camera ends it.
- **The update icon should show without a mower**, even when the mower is offline.


## Every language as fast as English

In any language other than English, the Toolkit could be very slow while a mower was connected — in the browser, on
Windows and in Home Assistant alike. The page should now respond as quickly as it does in English. It should also open
already in your language instead of switching after it loads, and it downloads its language file once instead of on
every visit.

## Keep the remote-control camera on

Remote → **Keep camera on**. With it on, the remote-control camera keeps running when the window is not in front, is
minimized or your phone is locked, instead of stopping to save data.

- Turning it on asks you to confirm: **you must stop the camera to end the session, or the mower stays in remote
  control.**
- The blades keep spinning only while the live picture keeps arriving.
- On 4G it uses cellular data the whole time.
- Off, the camera stops when the window is not on screen, as before.

## The update icon without a mower

The ⚠️ update icon should now appear even when the mower is offline or no mower is connected: the Toolkit checks when
the page opens or reconnects. Installing is unchanged — you choose, or automatic updates do if you turned them on.

## Several mowers

One mower losing its connection should no longer hold up the other mowers going to sleep or waking.

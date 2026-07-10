# Lymow Toolkit — Home Assistant Add-on

The full Lymow Toolkit dashboard, running as a Home Assistant add-on: live map with accurate
coverage paint, per-zone cutting settings, scheduler and calendar, freshness and RTK heat maps,
fault auto-recovery, mow history, remote control, and more — for the Lymow One robotic mower.

## Installation

1. In Home Assistant go to **Settings → Add-ons → Add-on Store**.
2. Open the **⋮** menu (top right) → **Repositories**, paste this URL, and click **Add**:

   `https://github.com/AppGuy77/lymow-toolkit-downloads`

3. Find **Lymow Toolkit** in the store list (refresh the page if it doesn't appear) and click
   **Install**. The add-on builds on your machine — the first install can take a few minutes on a
   Raspberry Pi. Later updates are much faster.
4. Click **Start**, then **Open Web UI** and sign in with your Lymow account (the same email and
   password as the official app). Prefer **"Sign in with Google"**? It opens an on-box browser
   right inside the dashboard (the add-on bundles Chromium for this) — sign in to Google there and
   it finishes on its own, no copy/paste.

## Updates

When a new toolkit version is released, Home Assistant shows an **Update** button on the add-on
page. Your login, settings, and backups are stored in the add-on's persistent data folder and
survive every update and rebuild.

## Notes

- **Port:** the dashboard listens on port 8787 (changeable on the add-on's Configuration tab under
  Network). Anything on your network can reach `http://<home-assistant-ip>:8787`.
- **Keep it running:** scheduled mows, fault auto-recovery, and history capture run from the
  add-on — leave it started (Start on boot is enabled by default).
- **HA Container / Core users:** add-ons require Home Assistant OS or Supervised. On plain
  Docker installs, run the standalone Docker bundle from the
  [latest release](https://github.com/AppGuy77/lymow-toolkit-downloads/releases/latest) instead —
  it is the same application.
- This is an independent community project — not affiliated with Lymow.

## Support

Questions and feedback: the [Lymow Toolkit Facebook group](https://www.facebook.com/share/g/1Jc7YfPStf/).

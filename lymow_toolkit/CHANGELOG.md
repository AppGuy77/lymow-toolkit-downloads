Lymow Toolkit v2.14.6

Run the Toolkit online, one phone link for every QR code and notification, and Settings restore fixes. It keeps your sign-in, settings, maps, layout and history — just update.


- **Run it online** — Northflank's free plan can host the Toolkit and updates it every night; the wiki has a step-by-step page and a ready template.
- **Phone link** — one address for every QR code and notification tap, and you choose it.
- **Back up & restore** — should no longer fail with "MemoryError".


## New

- **Run the Toolkit online — no computer that stays on needed.** Northflank's free Developer Sandbox plan can host it. The wiki's new page, *Run the Toolkit online (Northflank)*, walks through every screen with a picture, and a ready template for each of Northflank's regions creates the Toolkit with its own storage at /app/data, so the dashboard password, the Lymow sign-in and every setting survive restarts and updates. The template also sets up a nightly update: every night at about 3 AM in your region's time the Toolkit restarts on the newest version. For an update sooner, restart the service in Northflank.
- **Phone link: one address for every QR code.** The 📱 window, the phone section of the sign-in screen, Settings → Remote access and the push notifications' Address for phones all hand out the same address, picked in one place: **Automatic** (at home the away link, or the home-network address while away access is off; online the Toolkit's own https address), **This address** (the https address you opened the Toolkit with), **Home network** (for a phone on a VPN), **Away link** or **My own https address**. A tap on a push notification opens it.

## Changed

- **Push notifications: Address for phones is the phone link.** A custom https address you set before carries over. The list of phones shows any that turned notifications on at another address, so you know which to turn on again from the phone link.

## Fixed

- **Settings → Back up & restore should no longer fail with "MemoryError".** A restore asked the system for far more memory than it needed, which a machine that limits memory (a hosted plan) refused — for every backup, however small. The page then also showed "auth required" instead of the real error.
- **Restoring a backup should keep your notification switches.** A backup from an older version could come back with five notifications switched off.
- **A fresh install should open on the first mower in your list.** With two or more mowers it waited on "select mower" until you picked one.
- **Online (hosted) Toolkit:**
  - Google sign-in should work on a small plan.
  - The WiFi camera uses the direct link from any address — the Toolkit itself cannot reach your home network there.
  - The away link turns itself off; the Toolkit already has its own address.
  - Updates say to restart the service instead of offering an install the next restart would undo.

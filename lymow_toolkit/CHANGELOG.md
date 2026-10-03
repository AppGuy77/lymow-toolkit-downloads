Lymow Toolkit v2.9.0

An update for everyone on v2.8.6. It keeps your sign-in, settings, maps and history — just update.


- **Arrange the Overview and the Remote** — 🔒 Layout on the tab row: drag sections into rows, stack them in columns, resize them.
- **Remote control:** the arrow keys drive, **Show on camera** keeps what you hide hidden, and the WiFi picture should stay clean in fast motion.
- **The WiFi camera on an http:// address** (Home Assistant on your network) should work in Windows browsers and on iPhone.


## Arrange the page

- **🔒 Layout**, at the right end of the tab row, unlocks the Overview or the Remote. Every page load starts locked, so
  nothing moves by mistake, and leaving the page locks it again.
- Drag a section by its **⠿** handle. The marker says where it lands:
  - a **blue line across the row** (New row): a row of its own;
  - an **orange line on a section** (Same column): stacked in that section's column, above or below it;
  - an **orange outline** (Beside): a new column next to it — up to three columns in a row.
- Drag the edge between two columns to set their widths, and a section's bottom edge to set its height (double-click it
  to undo).
- The layout is saved on the Toolkit, so every browser shows the same page. A phone shows one column in the same order.
- **Reset layout** puts the page back the way it came.

## The dashboard

- Tiles fill the width, and tiles with more to say get more room. The dashboard is shorter than before at every screen
  size.
- **Minimal**, a switch in the dashboard header, shows one line per tile. Phones start Minimal; a phone and a computer
  each keep their own choice.

## Remote control

- **Arrow keys:** on a computer, ↑ drives forward, ↓ back, ← and → turn, two keys together drive an arc, and letting go
  stops the mower. Like the joystick, they work only with a live picture, at your Max drive speed, and never while you
  type in a field.
- **Show on camera** (Remote → Camera options): untick what you don't want on the picture — map toggles, Start · Dock ·
  Cancel, the task line, the readings bar, the mini map, the camera link buttons, the light button. It stays hidden; a
  tap doesn't bring it back. The blade buttons, Exit and fault messages always show. Phones and computers keep their own
  choice.
- **The WiFi picture should stay clean in fast motion.** It starts through the Toolkit as before, then switches to the
  mower's own direct WiFi link as soon as that connects, with the same delay. If the direct link can't connect, the
  picture stays as it was and the event log says why.
- **Smaller camera controls on big screens** — about a third smaller on a computer's fullscreen camera. Phones are
  unchanged.
- When a direct-WiFi or 4G picture drops, the joystick lets go at once and the mower gets one stop.

## The camera

- **On an http:// address** (Home Assistant on your network, or http://<address>:8787), the WiFi picture should come
  through the Toolkit in Windows browsers with no green picture, and iPhone and iPad should show it live instead of
  seconds behind.
- **The event log says what happened** for each camera start: which way was tried (WiFi through the Toolkit, WiFi
  direct, 4G), how it ended, why, and how long the first picture took. When the WiFi picture fails, it gives the camera
  helper's own reason.

## The map

- **Plot on Error** should place each fault where the mower was when it happened (marked ~ when that moment had no
  position and the last known one is used), plot every occurrence — the same fault at the same spot joins one pin, such
  as E16 ×3 — and keep the pins through reloads and restarts.
- A zone's label on a phone wraps and stays on screen.

## Windows and ports

- **Mower names in any alphabet work on Windows.** A name such as "Жук 2" no longer stops the camera, downloads or the
  event log, on Windows in any language.
- **The Toolkit keeps its address.** If 8787 is taken it uses the next free port (8788, 8789, then 8792–8799) and keeps
  it through restarts and updates; the local link, the phone QR code, the tray and the shortcuts follow it. Lymow
  Remote's 8790 and 8791 are never taken, and the installers open the port ranges in the firewall.
- On a non-English Windows the Toolkit no longer adds a duplicate firewall rule at every start.

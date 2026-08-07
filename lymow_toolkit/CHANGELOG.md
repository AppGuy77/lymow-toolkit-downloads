## v1.46.1 — the light stays on all the way to the dock


- 💡 The mower's light stays on for the whole drive back to the dock, so at night its camera can still see the dock's QR code


**Fixed**

- **The light was switched off as soon as the mower headed for the dock.** Since v1.44.2 it went out
  the moment the mower turned for home, which is exactly when it needs to see: the mower lines itself
  up on the dock using the QR code on it, and in the dark its camera cannot read the code with the
  light off. The light now stays on for the entire drive back, however long that takes, and goes off
  when the mower arrives — on the charger or waiting beside it.

Everything else is unchanged from v1.46.0. The light still does not come on when the mower goes out,
and the **Drive at night with lights** schedule works the way it always has.

---

**Update from inside the Toolkit** — the ⚠️ in the header, next to the 📖 — or download below.
**Docker/Unraid:** `docker compose pull`. **Home Assistant:** Update on the add-on page.

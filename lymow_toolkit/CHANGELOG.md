Lymow Toolkit v2.8.6

An update for everyone on v2.8.5. It keeps your sign-in, settings, maps and history — just update.


- **The WiFi camera should connect whenever the mower's WiFi works** — both WiFi ways are tried before 4G, and Windows browsers should no longer show a green picture.
- **A mower on its dock should stay there** — "Charging not detected" and a fault on the way home no longer send it back out to mow.
- **Settings → Connectivity:** a real **Stay connected all the time** switch and the official app's **Network priority**.


## The camera

- **WiFi should connect whenever the mower's WiFi works.** The Toolkit tries both WiFi ways — through the Toolkit, and
  the mower's direct link to your browser — each until a picture arrives, and the way that worked last time goes first.
  **Auto** uses 4G only when the mower's WiFi is down (it reports 4G and has no WiFi address), when its signal is below
  your **Settings → Camera** level, or when no WiFi way gives a picture. **WiFi only** never uses 4G; it keeps trying WiFi.
  A mower set to **4G Preferred** in the official app no longer counts as "WiFi off" while its WiFi works.
- **No green picture on Windows.** A Windows browser that opens the Toolkit at its http:// address (Home Assistant,
  Docker, Ubuntu or Mac install) should show the WiFi picture without the green screen, from the first start.
- **The mini-map should always show its mower.** The camera's mini-map shows the mower where it is, else where it was
  last seen (kept through restarts), else at its dock, and centers on it — in Fleet Mode too.
- **This page stays on its own mower.** Picking a mower on another screen, or opening the Home Assistant Remote card,
  should no longer change what this page shows.

## On the dock

- **Charging not detected (#51) on the dock** is no longer cleared and resumed. The mower stays on the dock and the
  event log says why: check the charging contacts, then clear the error.
- **A fault on the way home** is resumed on the way home — the mower should carry on to the dock, never back out to mow.
  A fault mid-mow still resumes the mow.

## Settings → Connectivity

- The section is now called **Connectivity** (was Remote & connectivity).
- **Stay connected all the time** is a real switch that shows whether it is on.
- **Network priority** — **WiFi preferred** or **4G preferred** — is the mower's own setting, the same as the official
  app's Settings → Network → Network Priority, for each mower. The Toolkit asks before switching and says when the mower
  has confirmed it.
- **Toggle 4G / cellular** is gone, in the Toolkit and in Home Assistant.

## Home Assistant

- Switching on **Allow Home Assistant to control the mower** asks: stay connected to the cloud, or just respond to
  commands.
- A Home Assistant command that does not run is an event-log line that says why.

## Event log

- A command that never reaches the mower, or that the mower does not follow, is an event-log line naming the command,
  who sent it and why. So is an auto-resume that could not be made.
- **31 more error codes are named** in the event log and in **Settings → Warnings & errors → Other faults**. They are
  not restarted automatically.

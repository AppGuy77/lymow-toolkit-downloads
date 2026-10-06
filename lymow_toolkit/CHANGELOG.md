Lymow Toolkit v2.10.3

Simpler cutting settings, camera Auto and remote-control fixes for everyone on v2.10.2. It keeps your sign-in, settings, maps, layout and history — just update.


- **Cutting settings are simpler:** Save asks Selected zones or All zones; Mow with unsaved changes asks Mow with changes, Mow as saved, or save and mow.
- **Your settings should stay as you set them:** saving to all zones no longer resets the mow order to Perimeter first, and a scheduled mow puts every setting back.
- **Camera Auto stays on WiFi through short stutters** — only your Settings → Camera rule switches it to 4G.
- **Remote control is safer:** a game controller that drops out stops the mower, and a camera restart never keeps it driving.
- **Only errors pop up in the middle of the screen**, and the Logs tab shows what matters to you.
- **More of the Toolkit in your language.**


## Cutting settings

- **Save** (one button in both panels) asks one thing when zones are selected: **Selected zones** or **All zones**. With nothing selected it saves to all zones. **All zones** gives every zone the settings you changed, including a zone that had its own value for one of them; its other own settings stay.
- **Mowing with changes you have not saved** asks **Mow with changes** (this mow only), **Mow as saved** (your changes stay unsaved), **Save to selected zones & mow** or **Save to all zones & mow**, and names the zones it will mow. A save never changes which zones are mowed: all zones are mowed only when none is selected. In Fleet Mode, with nothing selected, Mow still asks which mowers first.
- The old Global / Keep custom / Each zone's own / These Mower settings questions are gone, and Settings → **Send to other mowers** has one button, **Send to all zones**.
- Saving to all zones should no longer reset the mow order to Perimeter first, nor drop your perimeter laps, perimeter direction and cross-cut angle.
- A save made while the mower is mowing should no longer be lost; it is written at the next mow.
- A scheduled mow with its own settings should put every setting back afterwards — perimeter direction, both obstacle settings and settings set to zero used to stay changed.
- The change lists show the words the controls use (Random, Touch only, Outer discharge).

## Camera

- **Auto** leaves WiFi for 4G only by your Settings → Camera rule, judged over the last 3 seconds, so the WiFi picture's normal stutter no longer switches it. Each switch is in the service log with the reason and the numbers.
- Switching back to WiFi no longer flashes an old picture.
- Two screens on one mower: the WiFi picture's automatic upgrade no longer takes the camera from your other screen.
- iPhone on a plain http:// page: the live 4G picture (Auto) or a reason (WiFi only), instead of a picture running seconds behind.
- Camera messages (switching links, reconnecting) show on the camera's own status line; only errors pop up in the middle of the screen.

## Remote control

- A game controller that drops out mid-drive stops the mower; it moves again only after the stick returns to center. A pop-up mid-drive stops the mower.
- A camera restart never keeps the mower driving — a held joystick, arrow key or controller has to be pressed again.
- A stop the cloud link drops should be sent again once the link is back; a stop that reached the mower goes to the log only.
- The arrow speed is asked when you press Start, not after every WiFi/4G switch.

## Logs and connection

- The **Logs** tab shows the mower's work, commands and who sent them, faults and anything that did not take. Technical lines (cloud link, camera, light details) are in the downloaded file, for when you ask for help.
- A sleeping mower is no longer woken by the Toolkit's own retries or save checks — each wake is a new sign-in that can bump the official app off your account.
- A command that does not reach the mower says "the cloud link is not responding right now" instead of a technical error.

## Languages

- The new texts are translated, and short words (OK, On, Off and others) and the messages the server shows are no longer in English.

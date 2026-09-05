Lymow Toolkit v1.56.0

Everything below is a change from v1.55.0.


- New: the camera's signal levels are yours to set, per mower, under Settings → Camera — the WiFi signal at which WiFi only reconnects, an optional minimum 4G signal before each 4G retry, the rule Auto uses to leave WiFi for 4G (dropped frames per second, or a WiFi signal level, each with its own slider) and the WiFi signal at which Auto returns. A live line shows the mower's current WiFi and 4G readings; Restore defaults puts back exactly what the Toolkit did before.


## Camera signal levels, per mower

Until now the numbers that decide when the live camera reconnects, and when **Auto** switches between
WiFi and 4G, were fixed inside the Toolkit. A mower that works at -85 to -90 dBm at the far end of the
yard never got its camera back on its own, because the fixed -70 dBm gate never released. Under
**Settings → Camera** those numbers are now yours, **per mower**:

| Control | Default | What it governs |
|---|---|---|
| WiFi only — reconnect when the WiFi signal is at least | -70 dBm | After a lost picture in WiFi only mode, the Toolkit waits for the mower to answer on your network at this signal or better, twice in a row, then reconnects by itself. |
| Wait for a minimum 4G signal before each 4G retry | Off | Off: a lost 4G picture is retried every 5 seconds whatever the signal. On: each retry first waits for the mower's 4G signal to reach the slider it reveals (default -90 dBm). A mower that reports no 4G number still retries on time. |
| Auto — leave WiFi for 4G on | Dropped frames, 5 per second | Dropped frames judges the picture itself: two seconds in a row losing more than the slider's count against its own normal rate switch to 4G (the picture runs about 10 frames per second, so 5 is half of it). WiFi signal (dBm) judges the mower's reported signal: three readings in a row at or below the slider switch, and a signal already that low when the camera opens goes straight to 4G. A picture under 3 frames per second is always a reason to switch. |
| Auto — return to WiFi when the WiFi signal is at least | -70 dBm | While Auto is on 4G it checks every 8 seconds; two checks in a row at this signal or better bring the picture back to WiFi. Always kept at least 5 dBm above the leave level so Auto cannot flip back and forth — move one slider and the other follows, and the Toolkit says so. |

Every dBm slider runs from -95 to -65 dBm in 1 dBm steps with the value shown beside it. A **Right
now** line shows the mower's current WiFi and 4G readings — and, while an Auto WiFi picture is
running, its frame rate and dropped frames — so you set a level with the real number in front of you.
**Restore defaults** puts that mower back to the numbers above. The "WiFi signal too weak for video"
diagnosis follows your WiFi level too (5 dBm under it, so -75 dBm at the default).

The levels are saved on the Toolkit itself, so every browser and phone you sign in from uses the same
ones and an update keeps them. The defaults reproduce exactly what v1.55.0 did, so nothing changes
until you move a slider. The 5-second retry cadence, the no-picture-no-driving gate and the blade
guard are untouched.

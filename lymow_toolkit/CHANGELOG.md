Lymow Toolkit v2.14.3

Lymow One deck reset after Recharge & Resume and between zones, a calmer remote control, and security patches. It keeps your sign-in, settings, maps, layout and history — just update.


- **Lymow One** — the deck should go back to your mowing height after Recharge & Resume and after a channel crossing into the next zone.
- **Remote control** — the "mower did not move" notice should no longer pop up while driving fine, and the small map follows the mower again.
- **Cutting & scheduling** grows while its panels are open in an arranged layout, and **security patches**.


## Fixed

- **Lymow One: the deck should go back to your mowing height after Recharge & Resume.** A Lymow One that came back from charging kept cutting with its deck raised. Once the mower is back in the zone it was mowing, the Toolkit now pauses it, lowers the deck all the way, gives it a moment to settle and resumes the mow — the same steps that fixed it by hand in remote control. The Event log shows each one as **🛞 Lymow One deck reset**.
- **Lymow One: the same after crossing a channel into the next zone.** When the mower leaves one task zone through a channel and arrives in the next, the deck is reset the same way.
- **Remote control: the "mower did not move" notice should no longer pop up while the mower is driving fine.** Over 4G (and WiFi) a move that only waited inside the Toolkit was judged late and refused. A move is now judged from when it reached the Toolkit, against the connection's recent speed, so only a really late connection holds a move. The notice waits 3 seconds and shows in the camera's status line instead of over the picture — the "picture is behind" notice does too. A refused Stop still shows in the middle of the screen.
- **The remote control's small map keeps the mower centered again.** It stopped following the mower after the first move.
- **No more false "resumed — not commanded by the Toolkit" entries.** A status report that briefly left out the mower's state was read as the mower resuming by itself.
- **Cutting & scheduling grows to show everything.** In a layout you arranged with a set height for Cutting & scheduling, opening Cutting parameters, Multi-pass or Adjust cut angle offset squeezed it into that height behind a scrollbar. The box now grows while one of them is open and goes back to its set size when you close it.
- **Security patches.**

## Languages

The new messages are translated in all 15 languages.

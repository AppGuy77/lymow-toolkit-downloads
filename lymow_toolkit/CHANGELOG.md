Lymow Toolkit v1.49.0

Everything below is a change from v1.48.2.


- Fixed: when your Lymow sign-in expired, the Toolkit looked connected while nothing worked. It now says so and shows the sign-in screen.
- New: Stay signed in — save your Lymow password on this computer and never be asked again.
- Fixed: in fullscreen camera, Exit sat on top of the Eco button, and the controls covered the view. They now move aside and fade out while you drive.
- Fixed: the battery log recorded a finished mow as "on the dock, not charging". Mowing and recharging are now separate, with efficiency per mow.


## Fixed

**An expired sign-in looked like a broken Toolkit.** Lymow's cloud gives every sign-in a lifetime of
about a month — that is a setting on their account, and nothing here can extend it. When it ran out,
the Toolkit carried on as though it were signed in: the mower list failed, the buttons did nothing,
and if you were in the middle of using it, the official phone app quietly took over the account's
single cloud connection while the Toolkit sat showing "reconnecting…". The only cure anyone could
find was Log out and back in, because that is the one action that clears the saved sign-in.

The Toolkit now recognizes it, says **"Your token has expired, please re-login."**, and shows the
sign-in screen on its own — with your email and region already filled in, so you are typing a
password and nothing else. If it happens while you are watching, you are told within a second or
two rather than being left guessing. A dropped Wi-Fi link or a busy server is deliberately NOT
treated this way: those keep your session and retry, because signing you out over a blip would be
worse than the problem being fixed.

If you sign in with Google, the sign-in screen offers Google, and offers it in the form that
actually works where you are — the browser on the Toolkit's own machine, or the built-in sign-in
browser when you are on a phone or away from home. Your saved away-from-home link and QR code keep
working throughout, so you can sign in from wherever you are without touching the Toolkit machine.
Home Assistant dashboard cards say the Toolkit is signed out and where to fix it, instead of showing
buttons that no longer do anything.

**In fullscreen camera, the controls covered the picture.** The Exit button and the Eco blade button
were drawn in the same corner and landed on top of each other. The map switches sat across the grass,
and the Drive and Deck sliders floated well above the bottom edge with an uneven gap beneath them.

The Exit button now has its own space that the blade buttons cannot climb into, the map switches tuck
into the black bar beside the video where the picture leaves room, and the Drive/Deck bar sits at the
bottom edge, where the mower's own deck already blocks the view.

**The battery log recorded finished mows as dock time.** A mow that used 63% of the battery over two
hours appeared as "On the dock, not charging — 99% → 36%". The log only knew whether the mower was
charging, so everything else was filed as sitting on the dock — and that wrong entry was then
averaged into the "it loses about 3% an hour sitting on the dock" figure, making that wrong too.

Mowing, recharging and sitting on the dock are now three separate things.

## New

**Stay signed in.** On the sign-in screen, tick it and the Toolkit signs itself back in from then on
— the monthly interruption above simply stops happening. To do that it saves your Lymow password on
that computer, so it asks you to confirm first and tells you in plain words what protects it on that
machine. Windows and Mac hand it to their own built-in protection. Every other machine, including
every Raspberry Pi, ties it to that machine's own hardware, so a copied SD card, a copied folder or a
backup opens nothing anywhere else.

It is off by default, and undone at any time by unticking it on the next sign-in or by using Log out.
Google accounts cannot use it: there is no password to save, so Google asks again about once a month.

**Mowing efficiency and recharge times.** Each mow now shows what it cost — battery per hour, and how
much lawn that bought, in your own units — so you can see efficiency drift over a season instead of
guessing. Each recharge is a single line from where the mower docked up to full, reassembled from the
dozens of times a day the dock connects and disconnects. The dock's own idle drain keeps its own
figure, measured only from time genuinely spent parked.

**Controls that get out of the way.** In fullscreen camera, the controls fade out after a few seconds
with no touch, and using the joystick clears them immediately — driving is when you most need to see
where you are going. A tap on the picture brings them straight back, and a **Keep controls visible**
switch turns the fading off for good. The blade buttons, Exit and the live status line never fade:
a stop control on a machine with spinning blades stays where you can reach it.

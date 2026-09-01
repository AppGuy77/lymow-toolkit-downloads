Lymow Toolkit v1.54.1

Everything below is a change from v1.53.1.


- Download your mowing history: in Advanced Data → Mowing history you can now Copy it or save it as CSV or TXT — for Today, this week, the last 30 days, all of it, or a custom date range. The file has your lifetime totals, every mow (date, zones, area, %, time, battery), and a per-zone breakdown.
- Keep the camera on while you work in another window: the camera you open from the map has a new "Keep camera on" switch, so the live view stays up when the window isn't in front or is minimized instead of stopping. (On 4G this keeps using cellular data — turn it off when you're done.)
- iPhone sign-in fix: on iPhone/Safari (especially as a Home Screen app) tapping Log in could do nothing, because Safari auto-filled a hidden field with an invalid value that silently blocked the form. Sign-in now goes through.


## Download your mowing history

Open **Advanced Data → Mowing history**. There's a new **Export range** control — Today, This week,
Last 30 days, All, or a custom from/to — and **📋 Copy**, **⬇ CSV** and **⬇ TXT** buttons beside it.
The file is organized into three parts: your **lifetime totals**, **every mow** in the range (date,
zones mowed, area, %, time and battery used), and a **per-zone breakdown** with each zone's current map
settings. It's the same history the official app shows, straight from the Lymow cloud.

One note: the mower stores *which* zones each mow cut and its area/time/%, but not the settings it used
at the time, so the per-zone settings in the file are your **current** settings (labelled as such). A
big **All** export reads the whole cloud history, so it can take a little while — the buttons show a
spinner and stay disabled until it's ready, so one tap is all it takes.

## Keep the camera on while you work in another window

The camera you open from the map (the 📷 icon) used to stop after a few seconds whenever the window lost
focus or was minimized, to save data. Now it has a **Keep camera on** switch, in both the pop-up and its
fullscreen. Turn it on and the live view keeps running while you do something else, until you turn it
off, stop the camera, or close it. It only affects this camera, never remote control. **On 4G it keeps
using cellular data the whole time the window is hidden, so switch it off when you're done.**

## iPhone sign-in fix

On iPhone/Safari — especially with the Toolkit added to your Home Screen — tapping **Log in** could
appear to do nothing at all. Safari was auto-filling a hidden e-mail field with an invalid value, and a
hidden invalid field can't be shown to you to fix, so the browser quietly refused to submit the whole
form. That field is now switched off whenever it isn't in use, so sign-in goes through.

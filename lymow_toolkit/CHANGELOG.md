Lymow Toolkit v1.59.5

Everything below is a change from v1.59.4.


- **The Street map background works again.** OpenStreetMap's volunteer-run tile servers now refuse apps like the Toolkit, so with Satellite off the map showed an "Access blocked" tile instead of your streets. The Street map is now drawn from Esri's World Street Map, updated monthly, with road names and building outlines sharp at lawn zoom. The hybrid view with Satellite on is unchanged.
- **The add-to-home-screen banner on phones is gone.** The floating buttons already give one-tap access, and on iPhone the banner could only show instructions. Adding the Toolkit to your home screen is still offered from the phone QR window.


## Street map background

OpenStreetMap's tile servers are run by volunteers, and their usage policy does not allow an app that is
installed on thousands of computers to load map tiles from them. They began answering the Toolkit with an
"Access blocked" picture in place of every tile, so with **Satellite** off the map lost its streets.

The Street map background now comes from Esri's World Street Map, the same company whose satellite photos the
Toolkit already uses by default. It is updated monthly and drawn as vector data, so road names and building
outlines stay sharp at the zoom you use to look at a lawn. Nothing to set up: turn **Street map** on as before.

- The hybrid view — **Satellite** and **Street map** both on — is unchanged.
- The street map needs the internet and a browser with WebGL, which every current phone and desktop browser
  has. If a browser has none, the map says so and shows your zones on a plain background instead of a blank map.
- The imagery alignment you saved for the old street map is kept but not applied to the new one, because the two
  are positioned differently. Unlock, drag and lock once more if the new street map needs nudging.

## Phone banner removed

The bar at the bottom of the screen on phones that offered to add the Toolkit to your home screen is gone. The
floating buttons already give one-tap access to the mower, and on iPhone the bar could only show instructions.
The phone QR window still has the **Add to Home Screen** button for anyone who wants the icon.

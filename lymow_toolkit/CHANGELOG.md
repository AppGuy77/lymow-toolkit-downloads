Lymow Toolkit v2.14.8

Android Back button fixes. It keeps your sign-in, settings, maps, layout and history — just update.


- **Back on Android** — should ask "Leave the Toolkit?" every time, with no tap needed first.
- **Leave** — should now close the Toolkit.


## Fixed

- **Android: Back should ask "Leave the Toolkit?" every time, right from opening the Toolkit.** Before, it only asked after your first tap, so opening the Toolkit and pressing Back closed it. This works with the Back button and the edge swipe. Two Backs in a row without a tap still leave; browsers do not let a page block that.
- **Leave should now leave.** When the Toolkit was the first page you opened, Leave stayed on the Toolkit and the next Back closed it with no question. It now closes the Toolkit, or goes back to the page before it, and Back asks again the next time you open it.
- **iPhone: no question when there is nothing to go back to.** With the Toolkit as the first page of the tab, Back does nothing on an iPhone, so there is nothing to ask.
- **A phone in "Desktop site" mode gets the question too.**

Lymow Toolkit v1.59.0

Everything below is a change from v1.58.3.


- **Sign in with Apple.** A new **Sign in with Apple** button on the sign-in screen, next to Sign in with Google, for everyone whose Lymow app account is an Apple Account. Works on Windows, macOS, Ubuntu, Docker and the Home Assistant add-on, and from a phone or another PC, and finishes on its own.


## Sign in with Apple

The sign-in screen now has a **Sign in with Apple** button beside Sign in with Google. It signs in with the
Apple Account you use in the official Lymow app and works everywhere Google sign-in works: Windows, macOS,
Ubuntu, Docker and the Home Assistant add-on, and from a phone or another computer.

Apple asks for your Apple Account email and password, then the 6-digit code it shows on your iPhone, iPad
or Mac. At the computer that runs the Toolkit, Apple's own **Sign in with iPhone** option is offered as well.
From a phone, another computer, Docker or Home Assistant the sign-in page runs on the Toolkit machine and
is shown inside the dashboard, so there you sign in with email + password + code. Like Google accounts,
Apple accounts cannot use Stay signed in and ask again about once a month.

## Cancel sign-in really cancels

Pressing **✕ Cancel sign-in** on the in-dashboard sign-in window should now close it for good, instead of
the window reopening by itself a moment later.

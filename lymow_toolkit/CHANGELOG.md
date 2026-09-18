Lymow Toolkit v1.59.3

Everything below is a change from v1.59.2.


- **Your away address can no longer change with how you sign in.** v1.59.2 could switch a Toolkit to a duplicate mower-xxxx address issued to a second sign-in identity of the same Lymow account (email+password, Google and Apple count as separate identities in Lymow's cloud). The link service now recognizes the account by its verified email and always returns its original address; a Toolkit that was switched returns to the original on its next start.


## Your away address can no longer change with how you sign in

Lymow's cloud treats email+password, Google and Apple sign-ins to the same account as separate
identities, and the link service issued each identity its own mower-xxxx address. A Toolkit kept the address
it had saved for as long as it never asked the link service again, which is why a saved address carried
over through every update until now.

v1.59.2 added a re-registration that asks the link service again. On a Home Assistant add-on signed in
through a different method than the one its saved address was issued to, that request came back with the
other identity's address and the Toolkit adopted it. That was wrong, and this release fixes both sides:

- **The link service** recognizes an account by its verified email. All identities of the same account
  resolve to the account's original address, the one issued first, and no second address is ever issued
  for the same email.
- **The Toolkit** tells the link service which address it holds and refuses any change the service does not
  explain. The one accepted change is the return from a duplicate to the account's original address, which
  is logged in plain words. Every install checks its address once per start, so a Toolkit that was switched
  to a duplicate by v1.59.2 returns to the original address on its first start after this update.

Your saved phone link stays what it was. If a Toolkit shows a different mower-xxxx address than the one you
saved, update it and restart it once.

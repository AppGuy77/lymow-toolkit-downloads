Lymow Toolkit v1.52.1

Everything below is a change from v1.52.0.


- Home Assistant fix: if your machine's clock had drifted from the real time, the mower could sign in and then immediately show offline. The Toolkit now corrects for a wrong device clock when it connects, so this should no longer happen. If this was affecting you, please let me know the update clears it — and it is still worth checking your machine's time sync.


## Home Assistant connection fix (time sync)

Some Home Assistant users saw the mower connect and then immediately drop to **offline**, and
signing out and back in did not help. The cause was the machine's **clock**: the cloud connection
is time-stamped, and if the Home Assistant machine's time had drifted far enough from the real
time, the cloud rejected the connection even though the sign-in itself worked.

The Toolkit now measures how far the machine's clock is off and **corrects for it** when it
connects, so a wrong clock should no longer knock the mower offline. If your machine's time is off
by more than a couple of minutes, the add-on log now says so — the connection works either way, but
the real fix is to get the machine's time sync (NTP) working.

**Please help me confirm this.** I could not reproduce it on my own machine, so if you were
seeing the mower go offline on Home Assistant, let me know whether this update clears it for you.

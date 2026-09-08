Lymow Toolkit v1.56.3

Everything below is a change from v1.56.2.


- Fixed: the precision guard should no longer pause the mower seconds after it leaves the dock for "No fix" while the RTK receiver is Fixed. The mower's positioning flag reads "Single point" for 5 to 30 seconds after every departure, and sometimes mid-mow, while the receiver stays Fixed at centimeter precision; the fix is now judged from both readings everywhere it is shown, with a note when they disagree. The precision limit is unchanged and still pauses a real degradation.
- Fixed: phone notifications said "RTK base link dropped / restored" for the Toolkit's cloud connection to the mower. They now say "Cloud link to the mower dropped / restored".


## The precision guard and the RTK fix

After every dock departure the mower's positioning flag reads "Single point" for 5 to 30 seconds while the
RTK receiver stays Fixed at centimeter precision, and sometimes mid-mow. v1.56.2 judged that flag alone,
so with "Also pause on No fix" on it paused the mower seconds after it left the dock and, standing still,
never resumed; the official app, which reads the receiver, looked fine.

The fix verdict now comes from both readings: the flag, raised by the receiver's own fresh Fixed or Float
reading, which the guard asks for every few seconds. The status pin, the GPS / RTK card, the diagnostics
row, the RTK log (a new **Fix** column beside **Fix q**) and the Home Assistant RTK fix sensor all show the
same verdict, with a note when the two disagree, and the event log records when the receiver vouched for a
fix. The precision limit is unchanged and still pauses a real degradation.

## Phone notification wording

"RTK base link dropped / restored" was the Toolkit's cloud connection to the mower dropping and returning,
not the RTK base. The rows now say "Cloud link to the mower dropped / restored".

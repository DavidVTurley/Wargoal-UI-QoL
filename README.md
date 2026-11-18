# Shift War Goals — experimental prototype

Not publication-ready. This prototype tests whether Shift-click invokes the vanilla add action without navigating away. It does not implement automatic exit when no eligible goals remain. It has not been tested in game; ordinary click, duplicate charges, context, scroll and Shift handling are unverified. Use a disposable save.

Copy the `mod` folder into `Documents/Paradox Interactive/Victoria 3/mod/shift-war-goals-prototype`, restart the launcher, and enable it in a test playset. Launch in debug mode. Test one normal click and Shift-click on two eligible Revoke Claim targets, then inspect logs/error.log. Repeat for Conquer State. Back out manually if the list is empty. Stop testing if a click adds twice or exits unexpectedly.

Overrides: `gui/add_wargoal_panel.gui` in full, based on Victoria 3 1.15.1. Conflicts with other mods overriding that file. The original game installation is untouched. The metadata and Workshop publishing flow have not been verified in the launcher; provide a thumbnail and complete in-game testing before publishing.

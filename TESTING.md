# Testing the row-only experiment

Version under test: 0.2.0-experimental, Victoria 3 1.15.1. Use a disposable save and a playset with only this mod enabled. Tick boxes with `[x]` after a pass; write down failures or mark unavailable cases as skipped.

## Install

- [ ] Close the game and launcher. In `Documents/Paradox Interactive/Victoria 3/mod/shift-war-goals-prototype/gui`, remove the old `add_wargoal_panel.gui` from the installed mod copy. Do not remove the game's own file.
- [ ] Copy `mod/gui/00_shift_wargoal_row.gui` from the workspace into that installed `gui` folder. Copy the workspace `mod/.metadata/metadata.json` into the installed mod's `.metadata` folder, replacing the old metadata.
- [ ] Confirm the installed `gui` folder has `00_shift_wargoal_row.gui` and does not have `add_wargoal_panel.gui`. Restart the launcher, enable the prototype, and start the game in debug mode.

## Core war-goal checks

Start a diplomatic play, before war, with multiple eligible states and sufficient maneuvers. Record the initial maneuvers and compare against displayed costs.

- [ ] Normal-click an eligible Revoke Claim target: exactly one demand is added, the normal cost is charged and the game returns to the previous panel.
- [ ] Reopen Revoke Claim. Hold left Shift and click one eligible target: exactly one demand is added and the same target list remains open.
- [ ] Still holding Shift, select a different eligible target: it is added once and the first cannot be added again.
- [ ] Release Shift: nothing happens until another click. Normal-click an eligible target: it is added once and the game returns to the previous panel.
- [ ] Repeat a Shift-click using right Shift, and check cost and result.
- [ ] Repeat normal and consecutive Shift clicks with Conquer State. Record which goals and states were tested.
- [ ] Add two goals with Shift, then press Escape or Back: navigation works and both goals remain.
- [ ] In a play with multiple countries, confirm each goal retains the intended target and beneficiary.
- [ ] Scroll partway down a long list, Shift-click a target and note whether the position and nearby rows remain visible.
- [ ] Try an invalid or unaffordable target: no goal is added and no cost is charged. Note whether the game gives its normal feedback.

## Treaty article checks

Use Enforce Treaty Article when available. If no suitable article is available, mark the case skipped rather than passed.

- [ ] On an article requiring a further choice, normal-click opens that choice; Shift-click also follows the normal choice flow. Confirm no demand is added prematurely.
- [ ] On an article without an extra choice, test a normal click and then, in a fresh comparable situation, a Shift-click. Record whether the term is added once, the cost, and whether the picker remains open. The new shared type may change this behavior.

## Boundaries and diagnostics

- [ ] After the final eligible or affordable target is added with Shift, record what appears. Automatic exit is not implemented; an empty or disabled list is a known limitation, not a pass for automatic exit.
- [ ] Inspect `Documents/Paradox Interactive/Victoria 3/logs/error.log` after testing. Save relevant new errors with the actions that produced them; the base game may also log unrelated errors.
- [ ] Record game version, other active mods, tested countries and article names, and any unexpected behavior. Stop if one click adds or charges twice.

The committed full-panel version can be recovered from Git commit `ebbace3`; reinstall its `mod` folder and remove the row-only file when reverting. Do not enable both versions together.

# Shift War Goals

Add several war goals of the same type without reopening the selection list after each one.

## How to use

During a diplomatic play, open **Add War Goal** and choose a war-goal type. Hold **Shift** while clicking an eligible target to add that demand and keep the list open. Click normally to add a demand and return to the previous panel. Back or Escape leaves demands already added in place.

The game still controls eligibility, maneuver costs and the effects of each demand. Some treaty-article rows share this UI and may also respond to Shift-click.

## Known limitation

The picker does not close automatically when no eligible or affordable targets remain. Use Back or Escape to leave it.

## Compatibility

Built and tested with Victoria 3 **1.15.1**. The mod defines the `add_wargoal_item` GUI type in `gui/00_shift_wargoal_row.gui`; it does not replace the complete vanilla panel file. Other mods defining that same GUI type may conflict, and game updates that change the row may require an update. Multiplayer compatibility has not been independently verified.

## Manual installation

Copy the contents of the repository's `mod` folder into a folder under `Documents/Paradox Interactive/Victoria 3/mod/`, then enable it in a launcher playset. The installed folder must contain `.metadata/metadata.json` and `gui/00_shift_wargoal_row.gui`. When upgrading from the earlier prototype, remove its `gui/add_wargoal_panel.gui` first.

See [TESTING.md](TESTING.md) for the testing checklist. The user reported testing the checklist and accepting the observed effects; individual results were not recorded.

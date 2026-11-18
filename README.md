# Shift War Goals — row-only experiment

This experiment replaces the reusable `add_wargoal_item` GUI type using `gui/00_shift_wargoal_row.gui`. It does not override the whole vanilla panel file. It may affect treaty article rows and conflict with other mods defining the same type. The row is copied from Victoria 3 1.15.1; updates to that row may require a merge.

The user reports testing the checklist and accepting the observed effects. See TESTING.md for installation and the checklist. The previous tested version is recorded in Git commit `ebbace3`. The experiment does not implement automatic exit when no valid targets remain. Do not publish until tested.

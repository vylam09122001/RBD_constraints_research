# RBD_constraints_research

14-week procedural VFX research project: a Houdini Digital Asset (HDA) for optimized Rigid Body Dynamics constraint networking, paired with a documentation Wiki and simulation videos demonstrating constraint/material behavior.

See the "RBD Constraints" Claude project for the full working notes (project overview, feature specs, decisions).

## Folder structure

| Folder | Contents | Tracked in git? |
|---|---|---|
| `/hip` | Houdini scene files (`.hip`) | Yes |
| `/otls` | HDAs, saved in expanded/directory format for diffable git history | Yes |
| `/python` | Custom Python modules used by HDAs/scripts | Yes |
| `/wiki` | Wiki source content (constraint/material behavior docs) | Yes |
| `/packages` | Houdini package JSON(s) that put `/otls` and `/python` on `HOUDINI_PATH` | Yes |
| `/geo` | Cached/exported geometry | No (gitignored) |
| `/render` | Render output | No (gitignored) |

## Houdini project setup

This folder is meant to be used as a Houdini **Project** (sets `$JOB` to this path), which makes paths in `.hip` files portable and lets the package in `/packages` auto-load.

In Houdini: **File → New Project...** (or the folder-icon Project chooser next to the menu bar) → point it at this folder → name it `RBD_constraints_research`. Houdini will offer to create standard subfolders; the ones listed above already exist, so you can uncheck/skip duplicates it tries to add.

To make the `/packages/rbd_constraints_research.json` package auto-load, either:
- Copy/symlink `packages/rbd_constraints_research.json` into `$HOUDINI_USER_PREF_DIR/packages/` (e.g. `Documents/houdini22.0/packages/`), or
- Set the environment variable `HOUDINI_PACKAGE_DIR` to include this project's `packages` folder before launching Houdini.

## Version control

This is a git repository. `.hip` files and expanded HDA folders are tracked as text for readable diffs; `/geo` and `/render` are gitignored (regenerable output).

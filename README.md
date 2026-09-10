# RBD_constraints_research

A Houdini Digital Asset (HDA) for optimized Rigid Body Dynamics constraint networking, paired with a documentation Wiki and simulation videos demonstrating constraint/material behavior.

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

## Version control

This is a git repository. `.hip` files and expanded HDA folders are tracked as text for readable diffs; `/geo` and `/render` are gitignored (regenerable output).

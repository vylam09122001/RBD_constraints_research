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
| `/sim` | Houdini default — simulation caches | No (gitignored) |
| `/abc` | Houdini default — Alembic caches | No (gitignored) |
| `/flip` | Houdini default — flipbook/viewport playblasts | No (gitignored) |
| `/tex` | Houdini default — textures | Yes |
| `/scripts` | Houdini default — shelf/panel/editor scripts | Yes |
| `/comp` | Houdini default — composite networks/output | Yes |
| `/audio` | Houdini default — audio assets | Yes |
| `/video` | Houdini default — video assets | Yes |
| `/desk` | Houdini default — saved desktop/pane layouts | Yes |

## Version control

This is a git repository. `.hip` files, expanded HDA folders, and hand-authored assets (`scripts`, `comp`, `audio`, `video`, `tex`, `desk`) are tracked as text/source; regenerable cache and output folders (`/geo`, `/render`, `/sim`, `/abc`, `/flip`) are gitignored.

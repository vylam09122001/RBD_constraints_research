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
| `/sim` | Houdini default — simulation caches | No (gitignored) |
| `/abc` | Houdini default — Alembic caches | No (gitignored) |
| `/flip` | Houdini default — flipbook/viewport playblasts | No (gitignored) |
| `/tex` | Houdini default — textures | Yes |
| `/scripts` | Houdini default — shelf/panel/editor scripts | Yes |
| `/comp` | Houdini default — composite networks/output | Yes |
| `/audio` | Houdini default — audio assets | Yes |
| `/video` | Houdini default — video assets | Yes |
| `/desk` | Houdini default — saved desktop/pane layouts | Yes |

## Houdini project setup

This folder is meant to be used as a Houdini **Project** (sets `$JOB` to this path), which makes paths in `.hip` files portable and lets the package in `/packages` auto-load.

In Houdini: **File → New Project...** (or the folder-icon Project chooser next to the menu bar) → set **Project Path** to the parent folder (`D:/Thesis`) with **Project Name** `RBD_constraints_research`, so `$JOB` resolves to `D:/Thesis/RBD_constraints_research` (not a nested duplicate). Under **Project Folders (Default)**, uncheck **Houdini Digital Assets (`hda`)** — this project keeps HDAs in `/otls` instead, tracked in expanded/directory format for diffable git history. All other default folders (`geo`, `sim`, `abc`, `tex`, `render`, `flip`, `scripts`, `comp`, `audio`, `video`, `desk`) can stay checked; Houdini will create them alongside the folders already here.

To make the `/packages/rbd_constraints_research.json` package auto-load, either:
- Copy/symlink `packages/rbd_constraints_research.json` into `$HOUDINI_USER_PREF_DIR/packages/` (e.g. `Documents/houdini22.0/packages/`), or
- Set the environment variable `HOUDINI_PACKAGE_DIR` to include this project's `packages` folder before launching Houdini.

## Version control

This is a git repository. `.hip` files, expanded HDA folders, and hand-authored assets (`scripts`, `comp`, `audio`, `video`, `tex`, `desk`) are tracked as text/source; regenerable cache and output folders (`/geo`, `/render`, `/sim`, `/abc`, `/flip`) are gitignored.

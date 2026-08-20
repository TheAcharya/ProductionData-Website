# Roles

![Roles Settings](/assets/pd-roles-settings.png)

**Production Data**'s `Roles` panel lets you review and include or exclude the video and audio roles found in your Final Cut Pro project. Role settings in the active [Configuration](/user-guide/configurations) control which roles appear in the exported report.

Drop an `.fcpxml` or `.fcpxmld` file onto Roles, or drag a timeline / compound clip from Final Cut Pro. Tables appear only after a project has been loaded.

## Video and Audio Tabs

![Video and Audio Tabs](/assets/pd-roles-settings-01.gif)

- **Video** — lists video roles from the loaded project.
- **Audio** — lists audio roles from the loaded project.

Use `Enable All` or `Disable All` for the selected tab. Disabled roles are omitted only from **role-bearing** sheets in the same export:

- Selected Roles Inventory (and each per-role inventory tab)
- Markers
- Keywords
- Titles & Generators
- Video & Audio Effects
- Speed Change Effects
- Summary

Role exclusion does **not** filter `Transitions`, `Non-Standard Effects & Templates`, or `Media Summary`.

!!!info Info
Disable a role when you want matching Role ▸ Subrole rows dropped from those role-bearing sheets — not from Role Inventory alone. Empty Role ▸ Subrole fields are left as they are.

Long role names may appear truncated on per-role Excel inventory tabs (Excel’s 31-character sheet-name limit). Disabling that truncated Roles entry still omits the matching full-length Role ▸ Subrole rows on Selected Roles Inventory and the other role-bearing sheets above. On Video & Audio Effects, exclusion also matches full inventory Role ▸ Subrole names, bare main-role fields, and raw Final Cut Pro role ids.
!!!

## Automatic and Manual Mode

Behaviour depends on [Export Mode](/user-guide/general/#export-mode):

- **Automatic** [!badge text="Default"] — dropping a project on Roles switches to [Extract](/user-guide/extract) and starts the export.
- **Manual** — Roles stays open so you can review roles first. Switch to [Extract](/user-guide/extract) and press `Start Export` when you are ready.

!!!info Info
To update the roles list, load a project again.
!!!

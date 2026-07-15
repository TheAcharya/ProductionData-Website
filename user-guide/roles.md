# Roles

![Roles Settings](/assets/pd-roles-settings.png)

**Production Data**'s `Roles` panel lets you review and include or exclude the video and audio roles found in your Final Cut Pro project. Role settings in the active [Configuration](/user-guide/configurations) control which roles appear in the exported report

Drop an `.fcpxml` or `.fcpxmld` file onto Roles, or drag a timeline / compound clip from Final Cut Pro. Tables appear only after a project has been loaded.

## Video and Audio Tabs

![Video and Audio Tabs](/assets/pd-roles-settings-01.gif)

- **Video** — lists video roles from the loaded project.
- **Audio** — lists audio roles from the loaded project.

Use `Enable All` or `Disable All` for the selected tab. Disabled roles are omitted from the export.

## Automatic and Manual Mode

Behaviour depends on [Export Mode](/user-guide/general/#export-mode):

- **Automatic** [!badge text="Default"] — dropping a project on Roles switches to [Extract](/user-guide/extract) and starts the export.
- **Manual** — Roles stays open so you can review roles first. Switch to [Extract](/user-guide/extract) and press `Start Export` when you are ready.

!!!info Info
To update the roles list, load a project again.
!!!

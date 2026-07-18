# General Settings

![General Settings](/assets/pd-general-settings.png)

## Export Destination

### Destination

You can select your desired location by clicking on the Folder Icon. Upon right-clicking folder icon, **Production Data** will show the `Full Path` associated with said folder.

If no folder has been chosen, **Production Data** will display `Please select!` If the saved folder can no longer be found, `Missing Folder!` will be shown.

### Export Folder Naming

Each export is saved within a subfolder inside your chosen export destination. In order to mitigate conflicts and potential overwrites of previously generated reports, **Production Data** incorporates the project name and the current date and time within the folder nomenclature. The timestamp uses the `yyyy-MM-dd-HH-mm-ss` format. Consequently, each export yields a distinct and uniquely identified result.

!!!info Info
`My Project-2026-07-13-10-30-45`
!!!

### Export Mode

Select your desired Export Mode.

- **Automatic** [!badge text="Default"]
- **Manual**

In `Automatic` mode, **Production Data** begins the export as soon as a project is received. In `Manual` mode, the project is queued on [Extract](/extract) and you confirm the export with `Start Export` when you are ready.

In `Automatic` mode, dropping a project on the [Roles](/roles) tab will switch to [Extract](/extract) before the export runs.

The current mode is shown as a badge on [Extract](/extract). You can also switch modes from the File menu (`Switch to Manual Export` / `Switch to Automatic Export`) or by pressing `⌘` `⇧` `E` on your keyboard.

!!!info Info
**Production Data** processes one FCPXML project per action. Whether you drag and drop onto [Extract](/extract) or [Roles](/roles), choose a file with `Choose File`, use `File → Open…`, or open a project from Finder or the Dock, only a single project is accepted. If multiple files are offered at once, **Production Data** uses the first item only.
!!!

## Export Options

### Timecode Format

Select your desired Timecode Format.

- **HH:MM:SS:FF** [!badge text="Default"]
- **Frames**
- **Feet+Frames**
- **HH:MM:SS**

This setting controls how timeline time values appear in the Excel workbook.

### Exclude Disabled Clips

Checking `Exclude Disabled Clips` will prevent **Production Data** from including disabled clips in the report.

By [!badge text="Default"], disabled clips are included in the spreadsheet.

### Include Markers Outside Clip Boundaries

Checking `Include Markers Outside Clip Boundaries` includes markers whose start falls outside the host clip’s media range — markers Final Cut Pro hides from the timeline and Tags list — on the `Markers` sheet.

When enabled, the Markers sheet also gains a `Hidden` column: `✓` for markers outside clip boundaries and `✗` for markers inside. By [!badge text="Default"], those out-of-bounds markers are omitted and the `Hidden` column is not shown.

Enable this option when you need a complete marker inventory, including markers that are not visible in Final Cut Pro’s Tags. It only takes effect when `Markers` is enabled under [Sheets](#sheets).

!!!info Info
The `Hidden` column is not listed under [Columns](#columns). It appears only when this option is on and cannot be excluded like other workbook columns.
!!!

### Distinguish Original and Proxy Media

Checking `Distinguish Original and Proxy Media` separates missing original and proxy media into distinct columns on the `Media Summary` sheet, rather than combining them into a single Missing Media column.

By [!badge text="Default"], Media Summary uses one Missing Media column. Enable this option when you need to tell original and proxy media apart. It only takes effect when `Media Summary` is enabled under [Sheets](#sheets).

### Protect Sheets

Checking `Protect Sheets` applies worksheet protection to every sheet in the Excel workbook (`.xlsx`), including the cover sheet and all content sheets. This discourages accidental edits after export.

By [!badge text="Default"], sheets are not protected. Enable this option when you want a light edit lock on the spreadsheet. Excel still opens the file without a password, and anyone can turn protection off in Excel. This is an edit lock, not file-open encryption.

`Protect Sheets` applies to the Excel workbook only. PDF export is unaffected — use Preview’s Encrypt (or another PDF tool) if you need to password-protect a PDF.

### Create PDF Report

Checking `Create PDF Report` instructs **Production Data** to write a PDF report (`.pdf`) alongside the Excel workbook (`.xlsx`) for each export. Both files are saved in the same timestamped subfolder within your `Export Destination`.

By [!badge text="Default"], only the Excel workbook is exported. Enable this option when you need a shareable PDF for review or distribution. When enabled, **Production Data** exports `MyTimeline.xlsx` and `MyTimeline.pdf` in the same folder (for example, `My Project-2026-07-13-10-30-45/MyTimeline.xlsx` and `MyTimeline.pdf`).

The PDF report is generated from the same built report as the Excel export. The columns, sheets, role inclusions, timecode format, and clip filtering reflected in the PDF are determined entirely by the [Active Configuration](configurations/#make-active-configuration) selected in the toolbar or [Configurations](/configurations) panel.

**Production Data** does not maintain separate PDF-specific sheet, column, or role settings. Any change to `Sheets`, `Columns`, or `Roles` in the active Configuration applies equally to both the `.xlsx` and `.pdf` outputs for that export. This is intentional.

To produce a different PDF layout or column set, switch to or update the appropriate [Configurations](/configurations) before exporting.

!!!info Experimental
PDF export is experimental and optimised for A4 landscape. Tables paginate across pages and cell text may truncate. The Row column is included by default for traceability; exclude it the same way as in Excel. Matching sheet pages share a tint. For the complete dataset and column options, use the accompanying Excel (.xlsx) report.
!!!

<hr>

## Sheets

![](/assets/pd-general-settings-sheets.png)

By [!badge text="Default"], **Production Data** includes `Selected Roles Inventory` in the Excel report. This tab permits you to choose which worksheets are included in each export.

### Full Report

Turning `Full Report*` on enables every optional sheet below. Turning it off allows you to choose sheets individually.

### Report Sheets

- **Selected Roles Inventory** [!badge text="Default"]
- **Markers**
- **Keywords**
- **Titles & Generators**
- **Transitions**
- **Video & Audio Effects**
- **Speed Change Effects**
- **Summary**
- **Media Summary**

A summary of enabled sheets is also shown in the status bar on [Extract](/extract).

!!!info Info
`Media Summary` lists media files referenced in the project. **Production Data** does not read or copy your media files for this sheet.
!!!

### Label

![](/assets/pd-general-settings-sheets-copyright.png)

The `Label` section adds an optional copyright line to the report cover branding.

Checking `Copyright` includes your text on the Excel cover sheet and, when [Create PDF Report](#create-pdf-report) is enabled, on the PDF cover and centred in the PDF page footer. By [!badge text="Default"], no copyright label is exported.

Press `Edit Copyright` at the bottom of the Sheets tab to enter or change the text. Enter the string as typed — year, `©`, or any wording you prefer. **Production Data** does not insert a copyright symbol or year for you. When text is set, the current value is shown beside the button.

If `Copyright` is turned on while the text is empty, the editor opens so you can fill it in. Turning `Copyright` off keeps your saved text for later use but omits the label from the next export.

!!!info Info
Whitespace-only text is treated as empty and is not written to the report.
!!!

<hr>

## Columns

![](/assets/pd-general-settings-columns.png)

The `Columns` tab controls which columns appear on role inventory sheets in the Excel workbook. Use the table to turn individual columns on or off. Disabled columns are omitted from the export.

### Enable All

Pressing `Enable All` will check all column selections.

### Disable All

Pressing `Disable All` will uncheck all column selections.

<hr>

## Notification

![](/assets/pd-general-settings-notifications.png)

### Notification Frequency

**Production Data** seamlessly integrates with the native macOS Notifications framework, delivering timely alerts upon the successful completion of tasks.

Select your desired Notification Frequency.
- **Never**
- **When Export Finishes** [!badge text="Default"]
- **Each Report Step**

!!!info Info
`Each Report Step` notifies you as each enabled report sheet is built and when the spreadsheet is saved, followed by a notification when the export finishes. The number of notifications depends on which sheets you have enabled under `Sheets`.
!!!

### Show Progress on Dock Icon

By [!badge text="Default"] Progress Bar is shown on **Production Data**'s dock icon.

### Open macOS Notification Settings

![](/assets/pd-general-settings-notifications_macOS.png)

Select the `Open macOS Notification Settings` link to open macOS Notification Settings. Navigate to **Production Data** to manage notification settings.

!!!info Info
**Production Data** will only show up in the macOS Notification Settings solely after the initial prompting attempt. If **Production Data** is the focused application, notifications won’t make a sound or appear on the screen.
!!!

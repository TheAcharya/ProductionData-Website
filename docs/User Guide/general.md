---
label: General
icon: gear
order: -3
---
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

### Create PDF Report

Checking `Create PDF Report` instructs **Production Data** to write a PDF report (`.pdf`) alongside the Excel workbook (`.xlsx`) for each export. Both files are saved in the same timestamped subfolder within your `Export Destination`.

By [!badge text="Default"], only the Excel workbook is exported. Enable this option when you need a print-oriented, shareable PDF for review or distribution.

!!!info Info
When enabled, **Production Data** exports `MyTimeline.xlsx` and `MyTimeline.pdf` in the same folder (for example, `My Project-2026-07-13-10-30-45/MyTimeline.xlsx` and `MyTimeline.pdf`).
!!!

The PDF report is generated from the same built report as the Excel export. The columns, sheets, role inclusions, timecode format, and clip filtering reflected in the PDF are determined entirely by the **active Configuration** selected in the toolbar or [Configurations](/configurations) panel.

**Production Data** does not maintain separate PDF-specific sheet, column, or role settings. Any change to `Sheets`, `Columns`, or `Roles` in the active Configuration applies equally to both the `.xlsx` and `.pdf` outputs for that export. This is intentional.

To produce a different PDF layout or column set, switch to or update the appropriate Configuration before exporting.

When `Create PDF Report` is enabled and the export completes successfully, `Extract` displays an `Open PDF` action alongside `Open Spreadsheet` and `Show in Finder`. `Open PDF` opens the exported file in `Preview`. To open the PDF in another application, use `Show in Finder` and open the file with your preferred PDF reader.

!!!danger Experimental
PDF report export is experimental. This document is optimised for A4 landscape review and distribution. Column titles, cell values, and metadata may be truncated where they exceed the available page width or column layout limits. Wide tables are paginated horizontally into column sets and vertically across continuation pages. The Row column is repeated on every continuation and column-set page so row numbers stay traceable across the sheet. All pages that belong to the same workbook sheet share a subtle background tint and header accent colour so spanned sections remain visually grouped. For the complete, untruncated dataset, column customisation, and workbook formatting options, please refer to the accompanying Excel (.xlsx) report exported alongside this PDF.
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

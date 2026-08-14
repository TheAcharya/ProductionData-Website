# Creating Excel Spreadsheet

![](/assets/content-banner-excel.png)

## Configuration Setup

![Create Configuration for Excel](/assets/pd-create-excel-spreadsheet-01.gif)

1. [Create Your Configuration](/user-guide/configurations/#add-configuration).
2. Select your desired Export Destination by clicking on the [Folder Icon](/user-guide/general/#export-destination).
3. Select `Automatic` or `Manual` [Export Mode](/user-guide/general/#export-mode). `Automatic` [!badge text="Default"] begins the export as soon as a project is received.
4. Optionally, under [Sheets](/user-guide/general/#sheets), enable the report worksheets you need — or turn on `Full Report` to include every optional sheet.
5. Optionally, under [Columns](/user-guide/general/#columns), enable or disable the columns that appear on role inventory sheets.
6. Optionally, under [Export Options](/user-guide/general/#export-options), enable `Include Speed Change Settings in Role Inventory` or `Include Screenshots in Role Inventory` when you need those Role Inventory extras (screenshots are Excel only).
7. Return to Configurations to [Update Active Configuration](/user-guide/configurations/#update-active-configuration).

!!!info Info
By [!badge text="Default"], **Production Data** includes `Selected Roles Inventory` only. Sheet and column choices are optional — leave them as-is for a lean roles workbook, or tailor them for your deliverable before you save the Configuration.
!!!

### Optional Sheet Selection

![](/assets/pd-general-settings-sheets.png)

On the [Sheets](/user-guide/general/#sheets) tab, choose which worksheets appear in the Excel workbook (`.xlsx`):

- Turn on `Full Report` to enable every optional sheet at once, **or**
- Enable sheets individually — for example `Markers`, `Keywords`, `Titles & Generators`, `Summary`, or `Media Summary`

A summary of enabled sheets is also shown in the status bar on [Extract](/user-guide/extract).

### Optional Column Selection

![](/assets/pd-general-settings-columns.png)

On the [Columns](/user-guide/general/#columns) tab, use the table to turn individual columns on or off. Disabled columns are omitted from the export. Press `Enable All` or `Disable All` when you need a quick reset.

## Final Cut Pro to Excel Spreadsheet

<video controls width="1920">
  <source src="/assets/pd-create-excel-spreadsheet-02.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

<br>

1. Drag and drop your `.fcpxml` or `.fcpxmld` file onto [Extract](/user-guide/extract), or drag a timeline / compound clip from Final Cut Pro.
2. **Production Data** will begin the export.
3. **Production Data** will create an Excel workbook (`.xlsx`) in your Export Destination.

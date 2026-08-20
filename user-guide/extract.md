# Extract

![Extract Window](/assets/pd-main.png)

**Production Data**'s home panel, `Extract`, lets you provide a Final Cut Pro project and generate an Excel production report (`.xlsx`), with an optional PDF when enabled in [General Settings](/user-guide/general).

Following the creation of your [Configuration](/user-guide/configurations), select an `Export Folder`, then provide a project to Extract.

## Drag and Drop

![Extract Window](/assets/pd-main-01.gif)

Drag and drop an `.fcpxml` or `.fcpxmld` file onto Extract, or drag a timeline / compound clip directly from Final Cut Pro. You may also use a Finder text clipping that contains FCPXML. The drop overlay reads `Drop to Extract Metadata to Spreadsheet`.

Alternatively, click `Choose File` or press `⌘` `O` to select a file.

In `Automatic` mode, export begins as soon as a project is received. In `Manual` mode, confirm with `Start Export` when you are ready.

!!!info Info
**Production Data** processes one FCPXML project per action. If multiple items are offered at once, only the first item is used.
!!!

!!!info Info
If [Include Screenshots in Role Inventory](/user-guide/general/#include-screenshots-in-role-inventory) is on and **Production Data** cannot read the original or proxy media, it will ask you to `Choose Media Folder` before writing the Excel workbook — see [Choose Media Folder](#choose-media-folder).
!!!

## Choose Media Folder

After the report is built, **Production Data** may show `Choose Media Folder` if [Role Inventory screenshots](/user-guide/general/#include-screenshots-in-role-inventory) are on and it cannot read the original or proxy media — for example after dragging a timeline from Final Cut Pro (staged in Cache), when media lives on another volume, or when media sits inside a Final Cut Pro library (`.fcpbundle`).

The panel title is `Choose Media Folder`, the message is `Original media, proxy media, a Final Cut Pro library, or an enclosing folder.`, and the button is `Grant Access`. Select one of those, then press `Grant Access`.

- The folder that holds your original media
- The folder that holds your proxy or transcoded media
- The Final Cut Pro library (`.fcpbundle`) that contains or references those files
- A parent folder that contains the library or the media

After you grant original media, the same panel may appear again for unread proxy or transcoded media — even when the original files are already readable. Some formats, such as MXF or camera RAW, still need a readable proxy. Grant that second folder the same way. **Production Data** keeps every successful grant for that export.

If remaining files still cannot be read, **Production Data** offers `Choose Another Folder`, `Continue Without Remaining Screenshots`, or `Cancel Export`. Leftover cells stay blank if you continue; the rest of the workbook still exports. Cancelling the first `Choose Media Folder` prompt cancels that export. Closing the follow-up proxy prompt offers the same three choices.

!!!info Info
The [Export Folder](/user-guide/general/#export-destination) bookmark does not automatically cover source media. A media-folder grant is session-only for that export and is not saved under [General](/user-guide/general). A `.fcpbundle` may only *reference* external media — if screenshots stay blank, grant the actual original or proxy folder. See [Include Screenshots in Role Inventory](/user-guide/general/#include-screenshots-in-role-inventory) and [Troubleshooting](/troubleshooting#choose-media-folder--grant-access-appeared-during-export).
!!!

## Excel Sample Sheets

+++ Sheet 1
![Selected Roles Inventory](/assets/pd-excel-example_01.png)
+++ Sheet 2
![Titles](/assets/pd-excel-example_02.png)
+++ Sheet 3
![Video](/assets/pd-excel-example_03.png)
+++ Sheet 4
![Roles](/assets/pd-excel-example_04.png)
+++ Sheet 5
![Markers](/assets/pd-excel-example_05.png)
+++ Sheet 6
![Keywords](/assets/pd-excel-example_06.png)
+++ Sheet 7
![Titles & Generators](/assets/pd-excel-example_07.png)
+++ Sheet 8
![Video & Audio Effects](/assets/pd-excel-example_08.png)
+++ Sheet 9
![Summary](/assets/pd-excel-example_09.png)
+++

## PDF Sample Pages

+++ Page 1
![Selected Roles Inventory](/assets/pd-pdf-example_01.png)
+++ Page 2
![Titles](/assets/pd-pdf-example_02.png)
+++ Page 3
![Video](/assets/pd-pdf-example_03.png)
+++ Page 4
![Roles](/assets/pd-pdf-example_04.png)
+++ Page 5
![Markers](/assets/pd-pdf-example_05.png)
+++ Page 6
![Keywords](/assets/pd-pdf-example_06.png)
+++ Page 7
![Titles & Generators](/assets/pd-pdf-example_07.png)
+++ Page 8
![Video & Audio Effects](/assets/pd-pdf-example_08.png)
+++ Page 9
![Summary](/assets/pd-pdf-example_09.png)
+++

!!!info Info
Both the Excel and PDF visual report formats may change without prior notice. **Production Data** is powered by [OpenFCPXMLKit](https://github.com/TheAcharya/OpenFCPXMLKit) a free and open-source, experimental FCPXML parsing engine. As the framework is experimental and has not been tested against every edge case or the full complexity of real-world timelines, complete data coverage cannot be guaranteed, and some data would be incomplete or omitted.
!!!

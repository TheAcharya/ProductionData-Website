---
label: Extract
icon: home
order: -2
---
# Extract

![Extract Window](/assets/pd-main.png)

**Production Data**'s home panel, `Extract` Panel, lets you provide a Final Cut Pro project and generate an Excel production report (.xlsx), with an optional PDF when enabled in [General Settings](/user-guide/general).

Following the creation of your [Configuration](/user-guide/configurations), select an Export Folder, then provide a project to Extract.

## Drag and Drop

![Extract Window](/assets/pd-main-01.gif)

Drag and drop an `.fcpxml` or `.fcpxmld` file onto Extract, or drag a timeline / compound clip directly from Final Cut Pro. You may also use a Finder text clipping that contains FCPXML.

Alternatively, click `Choose File` or press `⌘` `O` to select a file.

In `Automatic` mode, export begins as soon as a project is received. In `Manual` mode, confirm with `Start Export` when you are ready.

!!!info Info
**Production Data** processes one FCPXML project per action. If multiple items are offered at once, only the first item is used.
!!!

## Excel Sample

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

## PDF Sample

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
Both the Excel and PDF visual report formats may change without prior notice. **Production Data** is powered by [OpenFCPXMLKit](https://github.com/TheAcharya/OpenFCPXMLKit), a free and open-source, experimental FCPXML parsing engine. As the framework is experimental and has not been tested against every edge case or the full complexity of real-world timelines, complete data coverage cannot be guaranteed, and some data would be incomplete or omitted.
!!!
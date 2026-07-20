# Troubleshooting

Below, you will find a comprehensive list of common issues users may encounter, accompanied by solutions to resolve them.

If you are still stuck after following these steps, open the logs (`Help` → `Open Logs`) and retain the log files from the Logs folder when seeking further help.

## How to access the logs in Production Data?

To access the logs for **Production Data**, navigate to the `Help` menu and select `Open Logs`.

This opens the Logs folder in Finder and writes a current snapshot of application activity to `productiondata_log.txt`. During parse and export, **Production Data** also writes `openfcpxmlkit_log.txt` in the same folder.

!!!info Info
Both files live under Application Support for **Production Data**. Share them only if you are comfortable doing so when requesting support — they may include project and file names from your machine.
!!!

## Failed to export completely”

![Failed to export completely](/assets/pd-troubleshooting_01.png)

**Production Data** cannot write the Excel workbook until you choose an export destination.

You will see this when:

- The Extract footer shows `Please select!` next to `Export Folder`
- You start an export (drop, `Choose File`, `File → Open…`, or `Start Export`) without a folder selected
- The alert reads `Failed to export completely` with the message `Please select a valid export folder.`

On [Extract](/user-guide/extract), click the folder control in the footer, or open [General Settings](/user-guide/general) → `File` and choose a destination under `Export Destination`. Select a folder you can write to (for example on your Mac, an external drive, or a mounted network volume). Confirm the footer no longer shows `Please select!` — it should display the folder name — then provide your project again, or press `Start Export` if you are in `Manual` mode.

!!!info Info
The export folder is remembered with a security-scoped bookmark. **Production Data** does not store a plain file path as the source of truth. If the volume is disconnected later, see [Missing Folder!](#export-folder-shows-missing-folder).
!!!

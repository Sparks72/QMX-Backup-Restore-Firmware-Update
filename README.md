# QMX Backup / Restore & Firmware Update

[![Launch the tool](https://img.shields.io/badge/%E2%96%B6%20LAUNCH%20THE%20TOOL-open%20in%20Chrome%20or%20Edge-2ea44f?style=for-the-badge)](https://sparks72.github.io/qmx-backup-restore/)

### ▶ [Open it now: sparks72.github.io/qmx-backup-restore]([https://sparks72.github.io/qmx-backup-restore](https://sparks72.github.io/QMX-Backup-Restore-Firmware-Update/)

A browser tool for the QRP Labs **QMX / QMX+**. It backs up every setting and restores it intelligently, and it can carry out the whole firmware update. There's nothing to install or download: click the link above in **Chrome or Edge** (Windows, Mac, Linux or ChromeOS), plug in your QMX, and click **Connect**.

## What it does

- **Backup:** reads all settings over CAT and saves them as a JSON file.
- **Smart Restore:** compares the backup with the radio and writes only the settings that differ. It skips settings the current firmware no longer has, matches band settings by band name (so backups move between QMX and QMX+), and never writes *Band version*.
- **Firmware update, no PuTTY needed:**
  - goes into update mode through the QMX terminal menu (System → Update firmware), finding items by name rather than by counting key presses, because the menus remember their position and change between versions
  - never presses Enter on anything containing "factory" or "reset", and stops on anything unexpected
  - backs up first, then writes the firmware file straight onto the QMX drive
  - **streamlined mode:** choose the firmware file and the tool does the rest, after a countdown with a STOP button; downgrades and re-installs get a warning and a longer countdown
- **Save terminal capture:** records exactly what the radio sent, for bug reports.

## How to use

1. Connect the QMX by USB and open **[the tool](https://sparks72.github.io/qmx-backup-restore/)** in Chrome or Edge.
2. Close PuTTY or any other program that's using the QMX's COM port.
3. Click **Connect** and pick the QMX's port.
4. To update the firmware: **Update Firmware…**, then follow the steps in the window. If the QMX drive doesn't appear on the PC, switch the QMX off and on.

## Notes

- It needs the Web Serial API, so it works in Chrome and Edge but not in Firefox or Safari.
- Tested on a QMX+ with firmware 1_04_010 to 1_04_015.
- It's a single HTML file, so you can also download `index.html` and open it locally. Device names in the port picker show more clearly on the GitHub Pages version.

73, Paul DJ0CU / G4ADF

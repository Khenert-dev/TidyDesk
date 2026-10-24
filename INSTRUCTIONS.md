# How to use TidyDesk

## Install and open

1. Download the Windows x64 installer from the official TidyDesk GitHub release. You do not need Python or the application source code.
2. If an older copy is running, right-click its system-tray icon and choose **Exit TidyDesk**.
3. Open the installer and finish Setup. It installs for your Windows account and adds a Start menu shortcut. A Desktop shortcut is optional.
4. Open **TidyDesk** from the Start menu. The developer popup appears once; choose **Continue**. **About TidyDesk** reopens it later.

The distributed build is unsigned. Verify the release checksum if you need to check download integrity; a checksum is not a publisher signature.

## Organize existing files

1. Choose **Add folder**, then **Browse** to the folder you want to organize.
2. By default, files go into category subfolders inside that folder. If you prefer another location, enable **Use a different output folder** and select an existing folder on the **same drive**.
3. Choose **Add and review**. Check each file's **Move to** destination.
4. Choose **Organize** to apply those moves. Closing the review moves nothing.
5. Later, choose **Review and organize** on the saved folder to repeat the process.

Example: a folder containing `lesson.pdf`, `lab.ova`, and `linux.iso` can become:

```text
Your folder/
  Documents/lesson.pdf
  Virtual Machines/lab.ova
  Disk Images/linux.iso
```

Only files directly inside the selected folder are considered. Existing subfolders stay in place. The **Left in place** tab explains files that will not move. A name collision gets a numbered filename rather than replacing an existing file.

## Automatically sort future downloads

1. Check your browser's download location and add that exact folder to TidyDesk. A custom folder such as Brave downloads may differ from Windows Downloads.
2. Turn on **Automatically sort new files** for that folder. Existing files still require a manual review.
3. Keep TidyDesk running. New or changed files must remain stable for at least 10 seconds and several checks. Partial downloads and files held by another program wait longer.

Closing the main window normally keeps the app in the system tray. Use **Pause** to pause automatic sorting, or right-click the tray icon to pause or exit. Without a system tray, closing the app exits it. Launching at sign-in is optional in Settings.

## Undo and stop watching

- After organizing, choose **Undo**, or open **History → Undo latest batch**. Undo restores the latest outstanding batch only when the recorded content still matches and the original name is free.
- If Undo reports a conflict, check History. The file stays in place; nothing is overwritten.
- To remove a saved folder, choose **Options → Stop organizing this folder**. This removes its configuration, not your files.
- To change the destination, use **Options → Folder settings**.

## Appearance and rules

Choose **Settings → Appearance → Theme → Light or Dark**. The choice is saved and applies to dialogs too.

In **Rules**, enable, edit, or reorder file categories. The first enabled match wins. Supported groups include documents, images, archives, installers, code/data, virtual machines such as OVA/VMDK, and disk images such as ISO/IMG. Enable **Other** to sort ordinary files without a more specific match; upgraded profiles may leave Other disabled until you choose it.

## If something stays in place

| What you see | What to check |
| --- | --- |
| No files to organize | The folder may be empty, contain only subfolders, or have no enabled matching rules. Check **Left in place**. |
| New download has not moved | Check the exact browser folder, the automatic-sorting checkbox, Pause, partial companions, and whether another program is writing to it. |
| Folder cannot be added | Source and output must be ordinary local folders on the same drive; watched folders cannot overlap. Network paths and links/junctions are excluded. |
| Hidden/private-key files stay put | These exclusions are intentional, including under Other. |
| The old interface still appears | Exit the older tray copy before opening the updated app. |
| An operation reports an error | Read **History** and check that the folder is available and writable. Do not publish raw logs containing personal paths. |

TidyDesk does not run installers, mount disk images, unpack archives, scan for malware, delete clutter, or recursively reorganize project directories. Preview unfamiliar rules first and keep backups of important files.

Uninstall through **Windows Settings → Apps**. Organized files and the app profile are retained. Configuration/history are stored under `%LOCALAPPDATA%/TidyDesk` and may contain private paths.

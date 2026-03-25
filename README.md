**SteamSweeper**

SteamSweeper is a Windows desktop application for scanning Steam library folders and identifying likely empty or leftover game installations.

**What It Does**
Automatically detects the Steam installation path from the Windows registry
Supports manual Steam or library path override (advanced use)
Scans a Steam library for folders that do not contain .exe files and ignores Steam shared/system folders
Moves selected folders to a backup location instead of deleting them immediately
Restores backed-up folders back into the active library when needed
Allows excluding specific folders from scanning

**How Paths Work**
SteamSweeper works with standard Steam library structures, including:
steamapps/common
custom Steam library folders
The application automatically resolves the selected path to the correct usable Steam library folder.
Manual path override should be used carefully.
⚠️ If you point the app to the wrong location, SteamSweeper may move or delete folders you did not intend to modify. If you are unsure what the selected path contains, do not use manual override.⚠️

**Important Behavior**
Folders starting with Steam are skipped by default. This includes folders such as Steamworks Shared, Steam Controller Configs, and SteamVR
The backup view allows you to uncheck items before permanent deletion

**Logging**
SteamSweeper writes activity logs in two locations:
In-app output panel
Daily log files inside Steam Sweeper Logs
Log files are automatically created in the active library folder, one file per day:

Steam Sweeper Logs\YYYY-MM-DD.log
Safety Notes

SteamSweeper is designed to be safe, but it performs real file system operations with administrator privileges.

**Recommended usage**

Review logs before deleting anything
Use backup instead of permanent deletion whenever possible
⚠️Avoid manual path override unless you fully understand the target library structure⚠️

**Permissions**
The application runs with administrator privileges because some Steam libraries may be located in protected directories such as Program Files.

**Build**
Requirements
Windows
.NET 8 SDK

**Author**
David Svitavský
Contact: SteamSweeperApp@gmail.com

**SteamSweeper**

SteamSweeper is a Windows desktop application for scanning Steam library folders and identifying likely empty or leftover game installations.

**What It Does**
Automatically detects the Steam installation path from the Windows registry
Supports manual Steam or library path override (advanced use)
Scans a Steam library for folders that do not contain .exe files and ignores Steam shared/system folders
Moves selected folders to a backup location instead of deleting them immediately
Restores backed-up folders back into the active library when needed
Allows excluding specific folders from scanning

<img width="1398" height="860" alt="image" src="https://github.com/user-attachments/assets/65d3ccce-1ce7-44cd-b92c-0b23c2bb0639" />

**How Paths Work**
SteamSweeper works with standard Steam library structures, including:
steamapps/common
custom Steam library folders
The application automatically resolves the selected path to the correct usable Steam library folder.
Manual path override should be used carefully.

⚠️ If you point the app to the wrong location, SteamSweeper may move or delete folders you did not intend to modify. If you are unsure what the selected path contains, do not use manual override.⚠️
<img width="1196" height="814" alt="image" src="https://github.com/user-attachments/assets/1db5a2ac-5797-4f02-bf55-e6cfeaf0f823" />

**Important Behavior**
Folders starting with Steam are skipped by default. This includes folders such as Steamworks Shared, Steam Controller Configs, and SteamVR
The backup view allows you to uncheck items before permanent deletion


**Logging**
SteamSweeper writes activity logs in two locations:
In-app output panel
Daily log files inside Steam Sweeper Logs
Log files are automatically created in the active library folder, one file per day:

Steam Sweeper Logs\YYYY-MM-DD.log

<img width="746" height="613" alt="image" src="https://github.com/user-attachments/assets/7bb5d243-801f-41dd-b2ed-d447e2dc5641" />

**Safety Notes**
Safety Notes

SteamSweeper is designed to be safe, but it performs real file system operations with administrator privileges.

For safety reasons, the following locations are permanently blocked and cannot be unlocked inside the app:

Drive root paths such as C:\, D:\, or E:\
Windows system folders and their subfolders
Users
ProgramData
$Recycle.Bin
System Volume Information
These protections also apply to manual library paths, backup paths, and file operations such as scan, backup, restore, delete, and log creation.
_(If there is interest, I can enable these features later, but for the first version, I think it’s safer not to do so.)_


<img width="355" height="159" alt="image" src="https://github.com/user-attachments/assets/5f179e1d-c7a8-44db-af22-1570544d378f" />


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

If you find my work useful, feel free to support me:
<a href='https://ko-fi.com/C0C31WMMPE' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi6.png?v=6' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

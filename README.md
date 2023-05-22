# DayZ Standalone - BatchWarden
## Description
BatchWarden is a feature-rich script designed to streamline the management of your DayZ server.
It automates crucial tasks such as starting the server, installing and updating Steam Workshop Mods, managing server files, monitoring for crashes, and creating regular backups. With this comprehensive script, you can ensure a smooth and uninterrupted gaming experience for you and your players.

## Key Features
1. **DayZ SA Server Launch:**
- The script provides a hassle-free server launch process, allowing you to quickly and easily start your DayZ server.

2. **Steam Workshop Mod Management:**
- With BatchWarden, installing and updating Steam Workshop mods becomes a breeze. The script automatically detects and downloads the latest versions of your desired mods, ensuring a seamless integration into your server.

3. **Server File Updates:**
- Staying up-to-date is crucial in maintaining a stable and enjoyable DayZ server experience. This script simplifies the process of updating server files, including game patches, configuration files, and other essential components.

4. **Automatic Crash Recovery:**
- In the event of a server crash or unexpected shutdown, BatchWarden takes charge. It automatically detects the crash and initiates the server restart process, minimizing downtime and ensuring uninterrupted gameplay for your community.

5. **Backup Creation:**
- Protecting your server data is paramount. The script provides an automated backup feature that regularly creates snapshots of your server files and relevant data. These backups are stored in a secure location, allowing you to restore your server quickly and effortlessly in case of emergencies or data loss.

6. **Customization and Flexibility:**
- BatchWarden offers a range of customizable options, allowing you to tailor the script to meet your specific server requirements. Whether it's adjusting backup frequency, managing mod lists, or fine-tuning server settings, this script provides the flexibility needed for optimal server administration.

---

With BatchWarden, you can focus on providing an exceptional DayZ gaming experience to your community without getting bogged down by tedious manual tasks. Automate mod installations, updates, server restarts, backups, and ensure your server runs smoothly and reliably. Experience a streamlined management process and enjoy peace of mind, knowing that your DayZ server is in capable hands.

## Configuration
## General Settings
```bat
:: Command window name
SET WINDOW_NAME="DayZ-Standalone-Server"

:: Enable/Disable shorts breaks/timeouts between messages
SET FAST_BOOT=true

:: Path to the DayZ-Standalone-Server folder
SET EXE_PATH="C:\dayz"

:: Name of executable
SET EXE="DayZServer_x64.exe"

:: Logical CPU cores
SET CPU_CORES=%NUMBER_OF_PROCESSORS%

:: Set the port number of the DayZ SA server. (Default is 2302)
SET PORT="2302"

:: Set the DayZ config file
SET CONFIG="serverDZ.cfg"

:: Can use a file path, with environment vars, such as C:\Users\%USER%\Documents\DayZServer
:: or a string to keep the logs where EXE_PATH is
:: For more info see: https://forums.dayz.com/topic/239635-dayz-server-files-documentation/?tab=comments#comment-2396561
SET PROFILE=ServerProfiles

:: Set a FPS limit for the server. (max is 200)
SET FPS_LIMIT=200

:: Set to true to enable, false to disable
SET USE_MODS=true
	:: Path to the modlist.txt
	SET MODLIST_PATH="C:\dayz\modlist.txt"

:: Set to true to enable, false to disable
SET USE_SERVER_MODS=false
	:: Path to the modlist_server.txt
	SET MODLIST_SERVER_PATH="C:\dayz\modlist_server.txt"

:: Extra launch parameters
:: For more info see: https://community.bistudio.com/wiki/DayZ:Server_Configuration
:: In general, these parameters do not need to be adjusted
SET ADDITIONAL_PARAMETERS=-doLogs -adminLog -netLog -freezeCheck -filePatching
```
## Automatic Restart (optional)
## SteamCMD - Automatic Updates (optional)
```bat
:: Enable/Disable SteamCMD-Updater to update/download mods and server files
SET USE_STEAMCMD_UPDATER=false

:: This feature will sync all the *.bikey keys from each mod with the server keys folder
SET USE_KEY_SYNC=true

:: Path to the SteamCMD folder
SET STEAMCMD_PATH="C:\Program Files\steamcmd\"

:: Name of the executable
SET STEAMCMD_EXE="SteamCMD.exe"

:: Name of the Steam account that SteamCMD uses
SET ACCOUNT_NAME="YourSteamAccount"

:: Path to the Update/Download folder
:: The update folder is only used to download mods
:: and synchronize them with the existing server files
SET UPDATE_FOLDER_PATH="C:\dayz\0-updates"
```
## BattlEye-Extended-Controls (optional)
```bat
:: Enable/Disable BattlEye-Extented-Controls to monitor the server
SET USE_BEC=true

:: Path to BattlEye-Extended-Controls folder
SET BEC_PATH="C:\dayz\BEC\"

:: Name of the executable
SET BEC_EXE="Bec.exe"
```
## DayZ SA - Launcher (optional)
## Automatic Backups (optional)
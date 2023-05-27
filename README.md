# DayZ Standalone - BatchWarden
## Description
DayZ-BatchWarden is a feature-rich script designed to streamline the management of your DayZ server.  
It automates crucial tasks such as starting the server, installing and updating Steam Workshop Mods,  
managing server files, monitoring for crashes, and creating regular backups.  
With this comprehensive script, you can ensure a smooth and  
uninterrupted gaming experience for you and your players.

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
:: DEFAULT -> DEBUG=false
SET DEBUG=true

:: Command window name (optional)
:: DEFAULT -> WINDOW_NAME="DayZ-BatchWarden"
SET WINDOW_NAME=""

:: Path to the DayZ-Standalone-Server folder (optional)
SET SERVER_PATH=""

:: Name of executable (optional)
:: DEFAULT -> DAYZ_EXE="DayZServer_x64.exe"
SET DAYZ_EXE=""

:: Logical CPU cores
:: DEFAULT -> CPU_CORES="%NUMBER_OF_PROCESSORS%"
SET CPU_CORES=""

:: Set the port of the DayZ-Standalone-Server (optional)
:: DEFAULT -> PORT="2302"
SET PORT=""

:: Set the DayZ config file (optional)
:: DEFAULT -> CONFIG="serverDZ.cfg"
SET CONFIG=""

:: Set a path for your profiles folder (optional)
:: DEFAULT -> PROFILE="!SERVER_PATH!\1-Profiles"
SET PROFILE=""

:: Set FPS limit for the server. (optional)
:: (max: 200)
:: DEFAULT -> FPS_LIMIT="200"
SET FPS_LIMIT=""

:: Set to true to enable, false to disable (optional)
SET USE_MODS=true
	:: Path to the modlist.txt (optional)
	SET MODLIST_PATH=""

:: Set to true to enable, false to disable (optional)
SET USE_SERVER_MODS=false
	:: Path to the modlist_server.txt (optional)
	SET MODLIST_SERVER_PATH=""

:: Extra launch parameters (optional)
:: For more info see: https://community.bistudio.com/wiki/DayZ:Server_Configuration
:: In general, these parameters do not need to be adjusted
SET ADDITIONAL_PARAMETERS="-doLogs -adminLog -netLog -freezeCheck -filePatching"
```
## Automatic Restart (optional)
## SteamCMD - Automatic Updates (optional)
```bat
:: Enable/Disable SteamCMD-Updater to update/download mods and server files (optional)
SET USE_STEAMCMD=true

:: Path to the SteamCMD folder (required)
SET STEAMCMD_PATH="C:\Program Files\steamcmd\"

:: Name of the executable (optional)
:: DEFAULT -> STEAMCMD_EXE="steamcmd.exe"
SET STEAMCMD_EXE=""

:: Name of the Steam account that SteamCMD uses (required)
:: It is highly advised that you use a separate Steam account
:: for the DayZ server if you choose to use this feature
SET ACCOUNT_NAME="YourSteamAccount"

:: Path to the Update/Download folder (optional)
:: The download folder is only used to download mods
:: and synchronize them with the existing server files
:: DEFAULT -> DOWNLOAD_PATH="!SERVER_PATH!\0-Download"
SET DOWNLOAD_PATH=""
```
## BattlEye-Extended-Controls (optional)
To use this feature, you need to [download](https://github.com/TheGamingChief/BattlEye-Extended-Controls/archive/refs/heads/master.zip) BEC.  
Detailed information can be found in this [repository](https://github.com/TheGamingChief/BattlEye-Extended-Controls). The author explains how to set everything up.  
If you are using BEC, we recommend that you to disable [Automatic Restarts](#automatic-restart-optional).  
With the [BEC-Schedulder](https://github.com/TheGamingChief/BattlEye-Extended-Controls/blob/master/Config/Scheduler.xml) you can create time-based actions, for example to warn your players about an upcoming restart or to execute commands like shutting down the server. BatchWarden detects the downtime and restarts the required services.  
Another important point is that the time to wait for the initialization of BEC must be adjusted to the server start time.  
This setting can be adjusted in the [config](https://github.com/TheGamingChief/BattlEye-Extended-Controls/blob/master/Config/Config.cfg#L139).  
```bat
:: Enable/Disable BattlEye-Extented-Controls (optional)
SET USE_BEC=false

:: Path to the BattlEye-Extended-Controls folder (optional)
SET BEC_PATH=""

:: Name of the executable (optional)
SET BEC_EXE="Bec.exe"
```
## DayZ SA - Launcher (optional)
not recommended, limited startup parameters.
```bat
:: Set to true to enable, false to disable (optional)
SET USE_DZSAL=false

:: Path to the DZSAL folder (optional)
:: DEFAULT -> DZSAL_PATH="!SERVER_PATH!"
SET DZSAL_PATH=""

:: Name of DayZ SA Launcher Mod Server exe (optional)
:: DEFAULT -> DZSAL_EXE="DZSALModServer.exe"
SET DZSAL_EXE=""

:: Extra launch parameters (optional)
:: For more info see command line parameters
:: section of: https://dayzsalauncher.com/#/tools
SET DZSAL_PARAMETERS=""

```
## Automatic Backups (WIP)
coming soon
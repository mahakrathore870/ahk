<div align="center">

# [![]AHK

***


Depending on which sections of my repo you intend to use will determine how much manual setup is required from the user; For indepth instructions on how to get started with my repo, alongside any important notices head [over to the wiki page](https://github.com/Tomshiii/ahk/wiki).  
There you will also find complete definitions of all scripts/functions of my repo, important prerequisite information that is required of the user before my repo will function as expected, as well as detailed [installation instructions](https://github.com/Tomshiii/ahk/wiki/Installation).

### AHK Version Information:
This repo is to maintain work on the `ahk v2.0` versions of my scripts.
> [!Caution]
> These scripts will not work in `ahk v1.1`
***

## Short Explanation:

#### [Libs]
In this section of the repo you will find a collection of lib files containing helpful functions, classes, GUIs & more! Some scripts rely on other lib files to function properly so make sure you pay attention to the top of each script, if it has any `#Include <lib\path>` then you will also need that file for the script to function properly!  
If you ever notice any inconsistencies in any scripts (say a script *should* have an include listed but it doesn't) please be sure to raise an issue here on github so I can get it fixed.

#### [Keyboard Shortcuts.ini/Keyboard Shortcut Adjustments.ahk]
An ini file/ahk script combo for defining all keyboard shortcuts for programs that are then used within other scripts. Having them defined separately in an ini file allows for easy swapping of hotkeys without needing to dig through each and every macro/function that uses it. You do NOT need to run this ahk file, it is [`#Include(d)`](https://lexikos.github.io/v2/docs/commands/_Include.htm) in all scripts that require it.

#### [My Scripts.ahk]
This script is the "central" script if you will. A lot of my windows scripts are here (and a hand full of scripts I use for editing).

This script will also go through a lot of important functions on boot. Some go through their function every boot of the script while some are more conditional. These `startup` functions are contained within a class `startup {` and are as follows;
- `generate()` - Handles creating a new `settings.ini` file each new release. The `settings.ini` file will be located in `A_MyDocuments \tomshi\`. These settings can be adjusted by right clicking on `My Scripts.ahk` and clicking `Settings` or by pulling up `settingsGUI()` (default hotkey is <kbd>win + F1</kbd>)
- `updateChecker()` - Checks github to see if there is a new version of my scripts available and can automatically download it for you as well as backup your current script directory
- `updatePackages()` Checks for updates to packages installed through the `choco` package manager
- `trayMen()` - Adds some tray menu items to the right click menu of `My Scripts.ahk`
- `firstCheck()` - Will check to see if this is the first time you're running my scripts and offer a helpful GUI to run you through a few things to get you going.
- `oldLogs()` - Will remove logs in `..\Logs\Error Logs\` & `..\Logs\Other Logs\` older than 30 days
- `adobeTemp()` - Will scan your adobe temp folders and delete them if they're larger than the user adjustable setting. This function also contains a custom folder for `After Effects` and will require the user to meddle with it for full functionality
- `adobeVerOverride()` - Will optionally check the user's current `Adobe Premiere` and `Adobe After Effects` installed `.exe` files to ensure the version number lines up with what they've set in `settingsGUI()`
- `libUpdateCheck()` - Will check all external lib files to see if they're up to date
- `updateAHK()` - Will check for and alert the user of a new version of AutoHotkey
- `monitorAlert()` - Will alert the user of any changes to their monitor layout so they can be aware that some hotkeys might not work as expected


```
***
> [!Tip]
> Plenty more scripts can be found within this repo, feel free to check out the [wiki page](https://github.com/Tomshiii/ahk/wiki/Home) or just browse around for more!

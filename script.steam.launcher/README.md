# Steam Launcher

Start Steam Big Picture Mode from within Kodi

See Kodi forum thread for more details:
http://forum.kodi.tv/showthread.php?tid=157499

https://github.com/teeedubb/teeedubb-xbmc-repo
http://store.steampowered.com/bigpicture
http://kodi.tv/

---

## Development

- Enable Debug Logging in Kodi to see if there are any issues with the add-on. (https://kodi.wiki/view/Log_file/Easy)

### Windows

How to compile the AHK script to an `.exe` file for use with the add-on after modifications.

1. [Download v1 of AutoHotkey](https://www.autohotkey.com/download/)
1. [Download the Portable version of SciTE4AutoHotkey](https://www.autohotkey.com/scite4ahk/)
   - In order to debug the script, SciTE4AutoHotkey assumes the AutoHotkey binary is one level above it's folder, so create a symlink to the actual binary.
      ```sh
      # In the folder that contains the portable SciTE4AutoHotkey folder, run the below, but change <VERSION> to the version you installed.
      mklink .\AutoHotkey.exe "C:\Program Files\AutoHotkey\<VERSION>\AutoHotkeyU64.exe"
      ```
   - Within SciTE4AutoHotkey, open the `steam-launcher.ahk` file.
   - Add file arguments via `View > Parameters`, and add all the arguments in the first input (you don't have to add all of them individually).
   - Ensure you change the revision number in the AHK script to prevent your modified files from being overwritten during add-on updates.
   - After you've made your changes, compile it into an `.exe` by opening Ahk2Exe.
      ```
      Source: <PATH_TO_SCRIPT>
      Destination: <KODI_USERDATA>\addon_data\script.steam.launcher\scripts\steam-launcher.exe
      Custom Icon: <PATH_TO_ICON>
      ```
      Click **Convert**
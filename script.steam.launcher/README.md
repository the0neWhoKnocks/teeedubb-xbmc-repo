# Steam Launcher

Start Steam Big Picture Mode from within Kodi

See Kodi thread for more details:
http://forum.kodi.tv/showthread.php?tid=157499

https://github.com/teeedubb
http://store.steampowered.com/bigpicture
http://kodi.tv/

---

## Development

- Enable Debug Logging in Kodi to see if there are any issues with the add-on.

### Windows

1. [Download v1 of AutoHotkey](https://www.autohotkey.com/download/)
1. [Download the Portable version of SciTE4AutoHotkey](https://www.autohotkey.com/scite4ahk/)
   - In order to debug the script, SciTE4AutoHotkey assumes the AutoHotkey binary is one level above it's folder, so create a symlink to the actual binary.
      ```sh
      # In the folder that contains the portable SciTE4AutoHotkey folder, run the below, but change <VERSION> to the version you installed.
      mklink .\AutoHotkey.exe "C:\Program Files\AutoHotkey\<VERSION>\AutoHotkeyU64.exe"
      ```
   - Within SciTE4AutoHotkey, open the `steam-launcher.ahk` file.
   - Add file arguments via `View > Parameters`, and add all the arguments in the first input (you don't have to add all of them individually).
   - After you've made your changes, compile it into an `.exe` by opening Ahk2Exe.
      ```
      Source: <PATH_TO_SCRIPT>
      Destination: <KODI_USERDATA>\addon_data\script.steam.launcher\scripts\steam-launcher.exe
      Custom Icon: <PATH_TO_ICON>
      ```
      Click **Convert**

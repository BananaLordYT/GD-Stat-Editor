# GD Stat Editor

A mod for Geometry Dash that lets you change your balances from a panel in the icon kit.

> **Warning:** using this while logged into your GD account can get you hidden or banned from the leaderboards. Use it offline or logged out. It only works on **Geometry Dash 2.2091**, and it is unofficial software that runs inside your game. Back up your saves first.

## Install on Windows

Open **PowerShell** and run this. If Steam is installed somewhere else, change the first line.

```powershell
$gd = "C:\Program Files (x86)\Steam\steamapps\common\Geometry Dash"
Invoke-WebRequest "https://drive.google.com/uc?export=download&id=1pDX_8owVXJPfz9vAajwNq0Ah2Z-sEL5E" -OutFile "$gd\GDStatEditor.asi"
Invoke-WebRequest "https://github.com/ThirteenAG/Ultimate-ASI-Loader/releases/latest/download/Ultimate-ASI-Loader_x64.zip" -OutFile "$env:TEMP\asi.zip"
Expand-Archive "$env:TEMP\asi.zip" -DestinationPath "$env:TEMP\asi" -Force
Copy-Item "$env:TEMP\asi\dinput8.dll" "$gd\XInput1_4.dll"
```

## Install on Linux

1. In Steam, open Geometry Dash, then **Properties → General → Launch Options** and set it to:
   ```
   WINEDLLOVERRIDES="xinput1_4=n,b" %command%
   ```
2. Open a terminal and run:
   ```bash
   GD="$HOME/.steam/steam/steamapps/common/Geometry Dash"
   curl -L -o "$GD/GDStatEditor.asi" "https://drive.google.com/uc?export=download&id=1pDX_8owVXJPfz9vAajwNq0Ah2Z-sEL5E"
   curl -L -o /tmp/asi.zip "https://github.com/ThirteenAG/Ultimate-ASI-Loader/releases/latest/download/Ultimate-ASI-Loader_x64.zip"
   unzip -o /tmp/asi.zip -d /tmp/asi && cp /tmp/asi/dinput8.dll "$GD/XInput1_4.dll"
   file "$GD/GDStatEditor.asi"
   ```
   The last line should say `PE32+ executable (DLL)`. If it says HTML or text, the download link isn't working.

If the folder isn't found, your Steam is installed somewhere else. Right-click Geometry Dash in Steam → **Manage → Browse local files** to find the real path, and use it in the `GD=` line.

If you have Geode installed, move its loader DLL out of the game folder first, or the two will conflict.

## How to use it

1. Launch Geometry Dash and open the **icon kit**.
2. Click the **gear button** at the bottom-left.
3. Use the sliders or the **+ / −** buttons to change your balances.

## Addons

To keep your data between launches, check out Save Keeper: https://github.com/BananaLordYT/GD-Stat-Editor-Saver

## Uninstall

Delete `GDStatEditor.asi` and `XInput1_4.dll` from the Geometry Dash folder. On Linux, also remove the launch option.

If the game hangs on "Launching" after a crash (Linux): `pkill -f GeometryDash.exe; wineserver -k`

Not affiliated with RobTop Games.

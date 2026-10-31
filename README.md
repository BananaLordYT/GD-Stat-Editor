# GD-Stat-Editor
A mod for Geometry Dash where you can change your balances.
# Inject the mod:

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

If the first command can't find the folder, your Steam is installed somewhere else. Right-click Geometry Dash in Steam → **Manage → Browse local files** to find the real path.

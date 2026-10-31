# GD Stat Editor

A mod for Geometry Dash that lets you change your balances from a panel in the icon kit.

> **Warning:** using this while logged into your GD account can get you hidden or banned from the leaderboards. Use it offline or logged out. It only works on **Geometry Dash 2.2091**, and it is unofficial software that runs inside your game. Back up your saves first.

## Install on Windows

Open **PowerShell** and run this. If Steam is installed somewhere else, change the first line.

```powershell
$gd = "C:\Program Files (x86)\Steam\steamapps\common\Geometry Dash"
Invoke-WebRequest "https://drive.google.com/uc?export=download&id=1pDX_8owVXJPfz9vAajwNq0Ah2Z-sEL5E" -OutFile "$gd\GDStatEditor.asi"
Invoke-WebRequest "https://github.com/ThirteenAG/Ultimate-ASI-Loader/releases/latest/download/Ultimate-ASI-Loader_x64.zip" -OutFile "$env:TEMP\asi.zip"
Ex

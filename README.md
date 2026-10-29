# GD-Stat-Editor
A mod for Geometry Dash where you can change your balances.
# Inject the mod:

# Windows Command Prompt: $gd = "C:\Program Files (x86)\Steam\steamapps\common\Geometry Dash"
Invoke-WebRequest "https://drive.google.com/uc?export=download&id=1Dc3ZfJa55d1w3Jj-Jv_i7FrcBfBx3ALX" -OutFile "$gd\GDStatEditor.asi"
Invoke-WebRequest "https://github.com/ThirteenAG/Ultimate-ASI-Loader/releases/latest/download/Ultimate-ASI-Loader_x64.zip" -OutFile "$env:TEMP\asi.zip"
Expand-Archive "$env:TEMP\asi.zip" -DestinationPath "$env:TEMP\asi" -Force
Copy-Item "$env:TEMP\asi\dinput8.dll" "$gd\XInput1_4.dll"

# Linux Terminal:
To inject the mod, first you need to go to your steam game and go to Properties - General - Launch Options and set it to: WINEDLLOVERRIDES="xinput1_4=n,b" %command%      Then run:
GD="$HOME/.steam/debian-installation/steamapps/common/Geometry Dash"
curl -L -o "$GD/GDStatEditor.asi" "https://drive.google.com/uc?export=download&id=1Dc3ZfJa55d1w3Jj-Jv_i7FrcBfBx3ALX"
curl -L -o /tmp/asi.zip "https://github.com/ThirteenAG/Ultimate-ASI-Loader/releases/latest/download/Ultimate-ASI-Loader_x64.zip"
unzip -o /tmp/asi.zip -d /tmp/asi && cp /tmp/asi/dinput8.dll "$GD/XInput1_4.dll"
file "$GD/GDStatEditor.asi" 

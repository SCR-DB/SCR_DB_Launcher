# SCR_DB Launcher

Offline save launcher for StarCraft: Remastered custom maps that use SCR_DB saves.
This repository only hosts the launcher **release builds**. No source code is published here.

## Download

1. Open **Releases** on the right and pick the newest launcher release (`SCR_DB Launcher v…`).
   - The **Supported map list** release (`maplist`) is not something to download. The launcher fetches that small signed file by
     itself when you open a map version it does not know yet.
2. Download `SCR_DB_Launcher_<version>.zip` and extract the **whole folder** somewhere like your Desktop or Documents.
   - Do not run the launcher from inside the zip file.
   - Do not put it under `C:\Program Files` (the launcher cannot write save files there).
3. **Add the launcher folder to your antivirus exclusions.** The launcher reads and writes StarCraft's memory to exchange save
   data, so some antivirus programs flag it by mistake.
4. Run `SCR_DB_Launcher.exe` from the extracted folder. Leave the other files and folders next to it as they are.
   - If Windows shows **"Windows protected your PC"**, click **More info → Run anyway**. The launcher is an unsigned program,
     so Windows shows this warning.

From v1.16.0, a map update usually does not need a new launcher: the launcher checks the signed supported map list online once
when it sees a new map version. Download a new launcher when its release is announced.

## Updating to a new version

1. Close the launcher you are using.
2. Extract the new version into a **new folder**.
3. Move the `Data` folder from the old launcher folder into the new launcher folder. Your saves carry over.
4. Start the game **only after** moving `Data`. If you enter a game with the new launcher before moving it, you start as a new
   character, and once that gets saved, the old `Data` will no longer be accepted.

## Verifying the download

Each release lists the SHA256 hash of its files. To check the file you downloaded, run this in PowerShell:


Get-FileHash .\SCR_DB_Launcher_<version>.zip -Algorithm SHA256


If the result matches the hash in the release notes, the file is intact.
Only use launchers downloaded from this repository's Releases page.

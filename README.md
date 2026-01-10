# Risk Of Rain 2 | DLC Unlocker via SmokeAPI (Windows Guide)

**Last updated:** January 10, 2026  
**Game version compatibility:** Works with current game build (post-Alloyed Collective release)  
**Tool:** SmokeAPI v4.1.x (latest stable as of early 2025)

**Important legal notice**  
This guide describes using a third-party DLC unlocker. This violates Steam's Subscriber Agreement. Use at your own risk — possible consequences include Steam account restrictions (rare for single-player games), issues with updates, or loss of online features.  
**All files of DLCs are already bundled in the base game** — no additional downloading is required after unlocking.

## Current DLCs (January 2026)

| DLC                        | AppID    | Release Date       | Main Content                              |
|----------------------------|----------|--------------------|-------------------------------------------|
| Survivors of the Void      | 1607890  | March 1, 2022      | Void Fiend, new stages, void items, etc.  |
| Seekers of the Storm       | 2306620  | August 27, 2024    | False Son, new survivors, items, stages   |
| Alloyed Collective         | 2781620  | November 18, 2025  | Operator + Drifter, drones, new stages, bosses |

## Requirements

- Legitimate copy of **Risk of Rain 2** in Steam (base game AppID: 632360)
- Steam running in online mode (at least for the first launch)
- Antivirus disabled / exception added for game folder (DLLs often flagged as false-positive)
- Visual C++ Redistributable 2022 x64 (usually already installed)

## Step-by-Step Installation (Recommended: Self-Hook Mode with version.dll)

1. **Download official SmokeAPI**  
   Go to: https://github.com/acidicoala/SmokeAPI/releases  
   Download the latest version (v4.1.x ZIP file — e.g. `SmokeAPI-v4.1.2.zip`)

2. **Extract files**  
   You need:  
   - `smoke_api64.dll` (64-bit version — Risk of Rain 2 is 64-bit)

3. **Locate game folder**  
   Default path:  
   `C:\Program Files (x86)\Steam\steamapps\common\Risk of Rain 2`

4. **Install using Self-Hook (most stable method)**  
   - Rename `smoke_api64.dll` → **`version.dll`** (this is the recommended and most reliable name)  
   - Copy `version.dll` into the game folder (next to `Risk of Rain 2.exe`)  
   → **Do NOT** replace or touch original `steam_api64.dll`!

5. **Create configuration file**  
   In the same game folder create new text file named exactly:  
   **`SmokeAPI.config.json`**  

   Paste the following content and save (use Notepad, encoding UTF-8):

   ```json
   {
     "$schema": "https://raw.githubusercontent.com/acidicoala/SmokeAPI/refs/tags/v4.1.2/res/SmokeAPI.schema.json",
     "$version": 4,
     "logging": true,
     "default_app_status": "unlocked",
     "override_dlc_status": {
       "1607890": "unlocked",
       "2306620": "unlocked",
       "2781620": "unlocked"
     }
   }

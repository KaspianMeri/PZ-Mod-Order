# PZ Leam's Collection - Mod Order/Setting pack - B42.20.4 - September 21 2026

Back up your existing files if you want to preserve your current mod order and settings!

## Installation

1. Subscribe to all the mods in the [collection](https://steamcommunity.com/sharedfiles/filedetails/?id=3484510193)
2. Download and unzip the archive from the release.
3. Back up your existing files (rename or move them out):
   - `pz_modlist_settings.cfg` to `OLDpz_modlist_settings.cfg`
   - `ModOptions.ini` to `OLDModOptions.ini`
   - `YourSandboxPreset` to `OLDYourSandboxPreset`
4. Copy the contents of the **Lua** folder into:

   `C:\Users\[YourName]\Zomboid\Lua`

5. Copy the contents of the **Sandbox Presets** folder into:

   `C:\Users\[YourName]\Zomboid\Sandbox Presets`

6. Launch Project Zomboid.
7. In **Solo/Local -> Own sandbox -> Saved Settings**, select **Customized** and pick `Leam's Sandbox` from the list.
8. Play

## Troubleshooting

If you see error codes on launch, verify your game files through Steam (or simply restart the game) — in my experience, these usually clear up on their own after that.

If errors persist, or the game crashes on load, unsubscribe from **all** your Project Zomboid Workshop subscriptions and resubscribe to only the mods in the collection. This is very often caused by a leftover mod that's still subscribed but no longer part of the mod list — it can conflict silently even if it's disabled in the in-game mod selection menu.

If problems persist despite these steps, unsubscribe from all your mods, uninstall and reinstall the game, then resubscribe to the collection. Note that a base game reinstall does **not** clear your Workshop content cache (`C:\Program Files (x86)\Steam\steamapps\workshop\content\108600`) — if a corrupted, outdated or leftover mod is causing the issue, you may need to manually delete that folder as well before resubscribing.

Separately, if none of the above resolves the issue, Project Zomboid may simply not be allocated enough RAM by default to run this many mods smoothly.

## Increasing RAM allocation (If necessary)

1. In your Steam library, right-click **Project Zomboid -> Manage -> Browse Local Files**, then open `ProjectZomboid64.json` in a text editor.
2. Find the line containing `-Xmx` (inside the `"vmArgs"` array) (e.g. `"-Xmx3072m",`) and change the number: `8192` for a light setup, `12288`–`16384` for a very large collection. Keep the trailing comma and the `m` suffix (m defines the memory usage in megabytes).
3. Save and relaunch. Note this file often resets after a Build 42 update, so you may need to redo this step regularly.

## About the files

- `pz_modlist_settings.cfg` — the recommended mod order for the collection.
- `ModOptions.ini` — per-mod in-game option toggles matching this setup.
- `Leam's Sandbox.cfg` — the sandbox preset tuned for this collection.

Feel free to edit any of them as you like. Nothing here is locked in.

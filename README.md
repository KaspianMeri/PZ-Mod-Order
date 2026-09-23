# PZ Leam's Collection - Mod Order/Setting Pack - B42.20.4 - September 22, 2026

This repository provides the recommended mod load order and configuration files for PZ Leam's Collection.

---

## File Descriptions

* `pz_modlist_settings.cfg` — Suggested mod load order.
* `ModOptions.ini` — Mod-specific settings used by the collection.
* `Leam's Sandbox.cfg` — Suggested Sandbox configuration.

Feel free to edit any of these files to suit your preferences.

---

## Setup Instructions

1. Subscribe to all mods included in the [collection](https://steamcommunity.com/sharedfiles/filedetails/?id=3484510193).

   Wait until Steam has finished downloading and updating all Workshop items before launching Project Zomboid.

---

2. Download and extract the latest archive from the Releases section.

---

3. Before replacing anything, back up your existing Project Zomboid configuration files if you want to preserve them.

   Keep copies of:

    `pz_modlist_settings.cfg`
    `ModOptions.ini`
    your current `Sandbox Presets`

   You can simply rename your existing files.

   For example:

    `pz_modlist_settings.cfg`
    renamed to `OLDpz_modlist_settings.cfg`

---

4. Copy the **`Lua`** folder into:

   C:\Users\[YourName]\Zomboid\

   Allow Windows to merge the folders and replace existing files if prompted.

---

5. Copy the **`Sandbox Presets`** folder into:

   C:\Users\[YourName]\Zomboid\

---

6. Launch Project Zomboid.

   Open the Mod Manager menu
   
   select the `Leam-B42` preset from the `--Choose preset--` dropdown.

---

7. Start a new game.

    Solo/Local

    Custom Sandbox

    Find the dropdown `Saved Presets`

    Select the `Leam's Sandbox` preset

    Follow the next steps until the new game starts.
    
---

## Troubleshooting

### Error messages or error codes on startup

If you encounter error messages or error codes when starting Project Zomboid:

1. Close Project Zomboid and launch it again.
2. If the problem persists, verify the integrity of the Project Zomboid game files through Steam.

---

### "Sorry, an unexpected error occurred"

If the game displays **"Sorry, an unexpected error occurred"**, try a clean Workshop reset:

1. Unsubscribe from all Project Zomboid Workshop mods.

2. Close Steam.

3. Remove the Project Zomboid Workshop content from:

    C:\Program Files (x86)\Steam\steamapps\workshop\content\108600\

4. Restart Steam.

5. Resubscribe only to the mods included in the collection.

6. Wait until Steam has finished downloading and updating all Workshop items.

7. Copy the `Lua` and `Sandbox Presets` folders from the downloaded release back into your `Zomboid` folder.

8. Launch Project Zomboid again.

This can be caused by corrupted, outdated, missing, disabled, or incompatible mods or dependencies, as well as leftover Workshop content from a previous modlist.

---

### Full reset

If the steps above do not resolve the issue, a complete Project Zomboid reset may be necessary.

1. Unsubscribe from all Project Zomboid Workshop mods.

2. Close Steam.

3. Uninstall Project Zomboid.

4. Remove the Project Zomboid Workshop content from:

    C:\Program Files (x86)\Steam\steamapps\workshop\content\108600\

5. Back up your saves, configuration files, and any other data you want to keep **outside** your `Zomboid` folder.

6. Remove the entire Project Zomboid user directory:

   C:\Users\[YourName]\Zomboid\

   > **Warning:** Deleting this folder will remove your local Project Zomboid user data, including saves, configuration files, presets, and other associated files. Make sure you have backed up anything you want to keep before deleting it.

7. Reinstall Project Zomboid.

8. Resubscribe to the collection.

9. Wait for Steam to finish downloading the Workshop content.

10. Reinstall the configuration files from this repository.

11. Launch Project Zomboid.

---

Separately, if the game runs out of Java heap memory while loading or playing with a large number of mods, increasing the `-Xmx` value may help prevent crashes caused by insufficient memory.

---

## Increasing Java Heap Allocation (When Required).

1. Press K in-game to display the game's memory information and monitor memory usage while playing.

2. In your Steam library, right-click **Project Zomboid -> Manage -> Browse Local Files**.

3. Open `ProjectZomboid64.json` in a text editor.

4. Locate the `-Xmx` JVM argument inside the `vmArgs` array. For example:

   `"-Xmx3072m"`

5. If you are experiencing memory-related crashes, you may increase this value. 

    `8192m` can be used as a starting point, not a mandatory minimum requirement.

    For a very large and heavy collection, consider increasing it to `12288m` or `16384m`.

    These values are not mandatory recommendations and should only be increased if you are actually experiencing memory-related crashes.

    Do not allocate your entire RAM to the Java heap; leave enough headroom for the OS, background apps, and the JVM's non-heap allocations.

6. Save the file and restart Project Zomboid.

    > **Note:** `ProjectZomboid64.json` may be reset or modified following a Build 42 update, so this change may need to be applied again after future updates.

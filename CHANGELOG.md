### **v3.5.0**
## **◆ Added**
- ➕ Added lodestone support for the normal compass — shows the bound lodestone's coordinates and the direction to it
- ➕ Added a separate "Lodestone broken" state with a real block check (lag-free — only in already-loaded chunks)
- ➕ Added the compass.use-lodestone-target option
- ➕ Added the compass.show-last-known-lodestone-when-broken option (show the last known coordinates instead of the "broken" label)
- ➕ Added the compass.format-preset option:
    - classic
    - compact
    - minimal
- ➕ Added the recovery_compass.format-preset option:
    - classic
    - compact
    - minimal
- ➕ Added the recovery_compass.keep-after-death option — the recovery compass is no longer dropped on death
- ➕ Added the messages.lodestone-broken string to the language files (ru / en)
- ➕ Added translatable distance units:
    - messages.meters
    - messages.kilometers
    - messages.unknown
- ➕ Added auto-update for config.yml — new keys are appended while existing settings are preserved
- ➕ Added auto-update for the language files lang/ru.yml and lang/en.yml

## **◆ Changed**
- 🔧 Bumped the plugin version and all configs to 3.5.0
- 🔧 config-version is now automatically synced with the plugin version on startup
- 🔧 Extended the normal compass logic with lodestone handling without losing the old behavior (coordinates, biome, direction, time, world)
- 🔧 The recovery compass and dual-mode now respect the format presets
- 🔧 The recovery compass distance now uses translatable units (m / km)

## **◆ Fixed**
- 🐛 Fixed: after a plugin update the old config.yml was not topped up with new keys (you had to delete the config manually)
- 🐛 Fixed: on an old language file the "Lodestone broken" label was shown in English
- 🐛 Fixed lodestone "broken" detection — Bukkit used to return the stored position even after the block was destroyed, so the "broken" state never triggered
- 🐛 Fixed leftover English strings by moving distance units (m / km / unknown) into the language files

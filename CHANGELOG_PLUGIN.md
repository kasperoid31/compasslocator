# [17/07/26 17:17] 
### **v3.6.0**

## **◆ Added**
- ➕ Added a clock HUD — hold a clock to see the in-game time, the day number, and the weather right in the action bar
- ➕ Added death and lodestone markers directly on the locator bar — a colored dot shows where you died (while holding a recovery compass) and where your compass's lodestone is
- ➕ Added a height hint to the recovery compass — an up/down arrow and the vertical distance to your death point
- ➕ Added a direction arrow to the recovery compass — points toward your death point based on where you're facing
- ➕ Added the option to hide low-health players from the locator bar — players at 20% health or below vanish from the bar until they heal
- ➕ Added per-world control for the locator bar — you can turn it off completely in specific worlds
- ➕ Added the `/cl info` command — shows what the plugin is, who made it, the version, and where to download it

## **◆ Changed**
- 🔧 Bumped the plugin version and all configs to 3.6.0
- 🔧 The clock works independently of the compasses — you can hold it alongside a compass or on its own
- 🔧 The recovery compass's height hint and direction arrow only kick in when you're in the same world where you died

> ℹ️ **Note:** the death/lodestone dots on the locator bar need the **PacketEvents** plugin installed on the server. Without it, everything else still works normally — those two dots just don't show up.

# [20/06/26 13:53]
### **v3.5.1**

## **◆ Added**
- ➕ Added support for Minecraft 26.2
- ➕ Added the `recovery_compass.persist-deaths` option — death points are saved to `deaths.yml` and survive a server restart
- ➕ Added cross-platform `keep-after-death` — the recovery compass is now kept on death on Spigot too, not only Paper

## **◆ Changed**
- 🔧 Bumped the plugin version and all configs to 3.5.1
- 🔧 Migrated the action bar from the deprecated BungeeCord chat API to **Adventure** (`sendActionBar(Component)`); legacy `§` color codes still work
- 🔧 Plugin version is now read via `getPluginMeta().getVersion()` with a safe fallback for older cores
- 🔧 `PlayerMoveEvent` now refreshes the action bar only on block-coordinate changes instead of every movement (including head rotation) — far fewer packets
- 🔧 Inventory events (`InventoryClickEvent` / `InventoryDragEvent`) now trigger a state recalculation only when a compass is actually involved (hand / slot / cursor), not on every click in any chest
- 🔧 `keep-after-death` now uses pure Bukkit API (items removed from drops and restored on respawn) instead of the Paper-only `getItemsToKeep()`

## **◆ Fixed**
- 🐛 Fixed an NPE that crashed the recovery compass every tick when the death world was unloaded or deleted — `getWorldName(...)` is now null-safe and returns "Unknown"
- 🐛 Fixed a crash on malformed format strings — `distance-format` / `time-formats` now run through a guarded `safeFormat(...)` that warns instead of throwing
- 🐛 Fixed the locator bar flickering for all players whenever someone equipped/unequipped a compass — `ensureWorldLocatorBarEnabled()` no longer re-applies `setGameRule(LOCATOR_BAR, true)` on every refresh (re-setting it broadcast a packet to every client in the world)
  
# [09/06/26 20:04] 
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

# [25/05/26 17:53] 
### **v3.4.0**
## **◆ Added**
- ➕ Added vanilla Locator Bar for the regular compass on Minecraft / Paper 1.21.6+
- ➕ The regular COMPASS can now simultaneously display the old actionbar and the locator bar
- ➕ Added a separate locator-bar section in config.yml
- ➕ Added a setting to choose who is shown in the locator bar:
   - everyone
   - normal_compass
   - any_compass
- ➕ Added additional locator bar settings:
   - force-world-gamerule
   - restore-gamerule-on-disable
   - visible-range
   - hidden-receive-range
   - equip-pulse-delay-ticks
   - unequip-restore-delay-ticks
   - unequip-final-refresh-delay-ticks
- ➕ Added locator bar target update settings
- ➕ Added compass.show-world setting
- ➕ Added settings.clear-actionbar-when-no-compass setting
- ➕ Added settings.send-death-reminder-on-join setting
- ➕ Added settings.update-actionbar-on-move setting
- ➕ Added settings.update-period-ticks setting
- ➕ Added config-version
- ➕ Added an extended debug section in config.yml
- ➕ Added new debug settings:
   - log-events
   - log-viewer-state-changes
   - log-target-state-changes
   - log-attribute-writes
   - log-actionbar-text
   - log-viewer-refreshes
   - status-targets-limit
- ➕ Added new commands:
   - /cl status [player]
   - /cl refresh [player|all]
   - /cl debug <on|off|toggle>
- ➕ Added new permission nodes for status, refresh and debug
- ➕ Added translation for biome sulfur_caves → Sulfur Caves

## **◆ Changed**
- 🔧 Completely reworked config.yml
- 🔧 Config has been translated into Russian
- 🔧 Added detailed comments, explanations and examples to the config
- 🔧 Restored the extended config header in a friendly style
- 🔧 Locator bar logic is now based on vanilla waypoint attributes without replacing the old actionbar
- 🔧 The regular compass no longer loses its previous functions when the locator bar is enabled
- 🔧 Improved the reload system and player state updates
- 🔧 Improved the structure of language files
- 🔧 Improved diagnostics and debug output
- 🔧 Improved description and readability of settings for regular users
- 🔧 Prepared a more user-friendly configuration for publication and support

## **◆ Fixed**
- 🐛 Fixed an issue where the locator bar might not appear or work unstable
- 🐛 Fixed an issue where the locator bar might not disappear after removing the compass
- 🐛 Fixed the logic for displaying players in the locator bar
- 🐛 Fixed a conflict between the locator bar and the old actionbar of the regular compass
- 🐛 Fixed the behavior of the regular COMPASS so it once again shows coordinates, biome, direction, and other old data
- 🐛 Fixed state updates on slot change, hand change, inventory clicks, drag actions, item drops, death, respawn, world change, player join and quit
- 🐛 Fixed config readability and clarity

# [16/05/26 17:20]
### v3.3.0
### ◆ Removed
- 🗑️ Removed unused Waypoint Range system
- 🗑️ Removed onPlayerRespawn handler
- 🗑️ Removed keep-alive mechanism
- 🗑️ Removed Folia support

### ◆ Added
- ➕ Added multilingual support
- ➕ Added language setting in config.yml
- ➕ Added setting for decimal places in coordinates
- ➕ Added debug-mode setting
- ➕ Added new icons

### ◆ Changed
- 🔧 Localization moved from config.yml to separate files
- 🔧 Update frequency changed from 20 to 10 ticks
- 🔧 New update logic
- 🔧 Color settings moved to language files
- 🔧 Time of day and other formats moved to language files

### ◆ Fixed
- 🐛 Fixed warnings during loading about existing language files
- 🐛 Code shortened

# [26/03/26 19:13]
### **v3.2.1**
### ◆ Added
- ➕ Added compatibility with all cores: Paper, Purpur, Spigot, Folia
> For Folia, it is recommended to use version 3.2.0!

# [26/03/26 17:27]
### **v3.2.0**
### ◆ Added
- ➕ Added use-short-directions setting — short direction names (N, S, E, W) instead of full ones
- ➕ Added display of time of day (Day/Night/Morning/Evening) with customizable icons
- ➕ Added keep-alive mechanism for action bar updates (once per second) to prevent it from disappearing
### ◆ Changed
- 🔧 Improved performance — updates only when data changes
- 🔧 Added head rotation support for direction updates

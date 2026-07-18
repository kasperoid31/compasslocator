# [20/06/26 14:02]
### **CompassLocator 3.4.1** — Forge
*(1.21.10)*

## **◆ Added**
- ➕ Added a configurable separator — the `compass.separator` symbol and `colors.separator` color are now read from the language file, so the `{sep}` divider can be restyled everywhere at once instead of being hard-coded
- ➕ Added an `auto` value for the `language` option — `resolveLanguage(...)` now follows the JVM/system language (`Locale.getDefault().getLanguage()`) and falls back to whichever bundled file actually exists
- ➕ Added death-point persistence — recorded death markers are now written to `death-markers.txt` and reloaded on startup, so the recovery compass survives a server restart

## **◆ Changed**
- 🔧 Bumped the mod and all bundled configs to 3.4.1
- 🔧 Reworked the waypoint-range attributes — `WAYPOINT_RECEIVE_RANGE` / `WAYPOINT_TRANSMIT_RANGE` are now driven by a transient `AttributeModifier` (added/removed by id) instead of overwriting the base value, so the mod no longer clobbers other mods' modifiers or leaves a stale range after the compass is unequipped
- 🔧 Reworked separator rendering — the filled format is normalized and split on the `{sep}` token (legacy `<sep-color><symbol>` is normalized to `{sep}` first) and re-joined with the configured separator; `{time}` and `{world}` are appended as their own `{sep}`-joined segments
- 🔧 Config reload from the in-game settings screen is now marshalled back onto the server thread via `server.execute(...)`, so `reloadAndRefresh()` runs thread-safely

## **◆ Fixed**
- 🐛 Fixed unreliable death capture — death points are now recorded through `LivingDeathEvent` → `onPlayerDeath(...)` (and immediately saved), instead of being missed when the player respawned
- 🐛 Fixed coordinate rounding — with `coordinate-decimals: 0`, `formatCoordinate(...)` now uses `Math.floor(...)` so negative coordinates round down correctly instead of truncating toward zero
- 🐛 Fixed the "dead" recovery option not getting a divider — it now appends the `{sep}` segment like the other fields
- 🐛 Fixed a cross-thread crash when reloading the config from the client screen — the refresh no longer touches server state off-thread

---

# [28/05/26 15:17]
### **CompassLocator 3.5.0** — Fabric
*(26.1-26.1.2)*

## **◆ Added**
- ➕ Added a new display mode — overlay (text to the right of the hotbar instead of the action bar) — configurable, disabled by default
- ➕ Added smart lodestone handling — shows the direction and coordinates of the lodestone, not just the player's facing direction — configurable, enabled by default
- ➕ Added saving of lodestone coordinates even after it's broken — configurable, disabled by default
- ➕ Added `keep-after-death` option for the recovery compass — configurable, disabled by default
- ➕ Added format presets — `classic` (default), `compact`, `minimal`
- ➕ Added a new settings screen — tabs, live preview, "Apply" button, 3 profile slots, and a help button
- ➕ Added automatic language detection for the settings UI

## **◆ Changed**
- 🔧 The config has been extended with new sections

## **◆ Fixed**
- 🐛 The recovery compass no longer disappears after death (if `keep-after-death` is enabled)
- 🐛 Lodestone now shows the correct direction
- 🐛 The overlay no longer shifts when text wraps

---

# [27/05/26 13:07 - 17:17]
### **CompassLocator 3.4.0** — Fabric & Forge
*(1.21.6, 1.21.7, 1.21.8, 1.21.9, 1.21.10, 1.21.11, 26.1-26.1.2)*

## **◆ Added**
- ➕ Ported CompassLocator 3.4.0 to Minecraft 1.21.6-26.1.2
- ➕ Added Fabric support
- ➕ Added Forge support
- ➕ Added in-game configuration screen
- ➕ Added mod icon and metadata

## **◆ Fixed**
- 🐛 Fixed locator bar refresh bugs
- 🐛 Fixed disappearing action bar
- 🐛 Fixed multiplayer synchronization issues
- 🐛 Fixed refresh/update logic issues
- 🐛 Fixed compass switching visibility bugs

## **◆ Optimization**
- ⚡ Improved locator refresh performance
- ⚡ Reduced server and client load

## **◆ Compatibility**
- 🔒 Preserved original CompassLocator mechanics
- 🔒 Preserved YAML config support
- 🔒 Preserved `lang.yml` support

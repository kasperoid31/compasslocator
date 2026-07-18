<div align="center">

<img src="https://cdn.modrinth.com/data/cached_images/028c729a257b8817fc93c931f769dab6f3efa248.png" alt="CompassLocator Banner" width="100%">

![Version](https://img.shields.io/badge/version-3.6.0-1E90FF?style=for-the-badge)
![Minecraft](https://img.shields.io/badge/Minecraft-1.21.6+-4C9A2A?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Paper%20%7C%20Spigot%20%7C%20Purpur-FF6B35?style=for-the-badge)
![Fabric](https://img.shields.io/badge/Fabric-1.21.6+-DBD0B4?style=for-the-badge&logo=fabric&logoColor=black)
![Forge](https://img.shields.io/badge/Forge-1.21.6+-orange?style=for-the-badge)
![Java](https://img.shields.io/badge/Java-21+-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)

[![Modrinth Plugin](https://img.shields.io/modrinth/dt/compasslocator?style=for-the-badge&logo=modrinth&logoColor=white&color=00AF5C&label=Plugin%20Downloads)](https://modrinth.com/plugin/compasslocator)
[![Modrinth Mod](https://img.shields.io/modrinth/dt/compasslocator-kasperoid?style=for-the-badge&logo=modrinth&logoColor=white&color=00AF5C&label=Mod%20Downloads)](https://modrinth.com/mod/compasslocator-kasperoid)
[![Telegram](https://img.shields.io/badge/Telegram-channel-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/prostoimpery)

</div>

---

## 📌 What is this?

**CompassLocator** is a plugin **and** client mod that adds useful compass information directly to the action bar. **The only tool that combines a compass, death compass, locator bar radar, and a clock HUD in one.**

No more opening F3. Just hold a compass and see:

- where you are
- which direction you're facing
- what biome you're in
- where you died last time
- what time it is (with a clock in hand)

---

## ✨ What does the compass show?

**Normal Compass**
- Coordinates (adjustable precision — integer or decimal)
- Current biome
- Cardinal direction (North/South or N/S — as you prefer)
- Time of day (optional)
- World name (optional)
- If the compass is linked to a lodestone — shows lodestone coordinates
- If the lodestone is broken — shows "broken" or last known coordinates (configurable)

**Recovery Compass**
- Where you last died (coordinates)
- Which world
- Time since death
- Distance to death location
- The marker indicates the point of your death in the locator bar (v3.6.0)
- Height difference (up/down arrow) to your death point (v3.6.0)

**Combined Mode**
- Hold a normal compass in one hand and a recovery compass in the other
- The action bar shows information from both at once

---

## 📡 Locator Bar (for 1.21.6+)

With a normal compass in hand, you can see other players on the radar (like a minimap). Range is configurable — up to the entire world.

**New in v3.6.0:**
- Death point markers on the locator bar (colored dot where you died)
- Lodestone markers on the locator bar (colored dot where your compass is bound)
- Hide low-health players from the radar (configurable)
- Per-world control — turn it off completely in specific worlds

---

## 🕐 Clock HUD (v3.6.0)

Starting from version 3.6.0, **CompassLocator** adds a **clock HUD** — hold a clock in your hand and see the in-game time, day number, and weather right in the action bar.

**Features:**
- Shows exact time (24h or 12h format — configurable)
- Displays the current day number
- Shows current weather (Clear / Rain / Thunder)
- Works independently of compasses — hold it alongside a compass or on its own
- Fully configurable: choose which info to show, toggle 24h format, use custom display presets, and more

---

## 🖼️ Screenshots

<div align="center">

| Normal Compass | Recovery Compass | Combined Mode |
|:---:|:---:|:---:|
| <img src="https://cdn.modrinth.com/data/cached_images/549992fee58de0cbf846a5c41790d109696338b6.png" width="250"> | <img src="https://cdn.modrinth.com/data/cached_images/7109d2b5cb0d9d55bbca0a893bf04ea4fb441116.png" width="250"> | <img src="https://cdn.modrinth.com/data/cached_images/74b1dc4dbafaf951057f09f72b9edf316fb99d12.png" width="250"> |

| Locator Bar | Death & Lodestone Markers |
|:---:|:---:|
| <img src="https://cdn.modrinth.com/data/cached_images/e0602b6da604d308cddcf8ef451dc6cb06271007_0.webp" width="250"> | <img src="https://cdn.modrinth.com/data/cached_images/3914c53badfb903cfa922ccb08735451f370f3bb_0.webp" width="250"> |

</div>

---

## 🎮 For Players

- Works right out of the box — just hold a compass
- Information only appears when you're holding a compass
- Recovery compass shows the way to your items after death
- Hold a clock to see the time, day, and weather without opening F3
- **Plugin version:** No need to download anything on the client (except for Locator Bar — that requires Minecraft 1.21.6+)
- **Mod version:** Works on Fabric and Forge (Minecraft 1.21.6 — 26.1.2)

---

## 🛠 For Server Admins

The plugin is highly configurable via `config.yml`:

- Which information is shown (coordinates, biome, direction, world, time)
- Coordinate precision (integer or decimal)
- Short or full cardinal directions
- Action bar update frequency
- Who is visible in Locator Bar (everyone / only compass holders)
- Enable/disable any module
- Language (Russian, English, or auto-detect)
- Clock HUD settings (time format, day number, weather)
- Recovery compass settings (height hint, direction arrow, markers on locator bar)
- And much more

---

## 📥 Installation

**Plugin (server):**
1. Download the `.jar` file
2. Put it in your `plugins/` folder
3. Restart the server
4. Done! (Optionally, edit `config.yml`)

**Mod (client):**
1. Download the `.jar` file for Fabric or Forge
2. Put it in your `mods/` folder
3. Launch Minecraft

---

## ⚙️ Requirements

**Plugin:**
- Minecraft 1.21+
- Paper / Spigot / Purpur (or compatible forks)
- Java 21

**Mod:**
- Minecraft 1.21.6 — 26.1.2
- Fabric or Forge

Locator Bar requires **Minecraft 1.21.6+** on the client.

---

<details>
<summary><b>🔄 There's also a client mod version!</b></summary>

A separate client-side mod for Fabric and Forge on Minecraft **1.21.6 — 26.1.2**.

Functionality will differ from the plugin (client-side capabilities are broader). Details — after release.

👉 [CompassLocator — Mod Version](https://modrinth.com/mod/compasslocator-kasperoid)

</details>

---

## ❓ FAQ

<details>
<summary><b>Do I need to install anything on the client?</b></summary>
For the plugin version — no. For the mod version — yes, the mod itself. For Locator Bar (plugin) you need Minecraft 1.21.6+ on the client.
</details>

<details>
<summary><b>What's the difference between the mod and the plugin?</b></summary>
The plugin runs on the server. The mod runs on the client. Functionality is similar but the mod has access to more client-side features.
</details>

<details>
<summary><b>Does the compass work in both hands?</b></summary>
Yes, you can hold it in either hand. Both are checked.
</details>

<details>
<summary><b>What if the compass is linked to a lodestone?</b></summary>
The plugin will show lodestone coordinates after your own coordinates. If the lodestone is broken, you can configure it to show the last known coordinates.
</details>

<details>
<summary><b>Does the recovery compass drop on death?</b></summary>
Configurable. If you enable the option, the compass stays in your inventory even on death (when keepInventory is disabled).
</details>

---

## 🔍 Поисковые теги / Search keywords

<details>
<summary><b>Click to expand</b></summary>

**Русский:** компас, координаты, направление, биом, радар, локатор бар, action bar, locator bar, компас смерти, death compass, recovery compass, точка смерти, магнетит, lodestone, навигация, стороны света, время суток, мир, часы, время в майнкрафт, F3, замена F3, текст над инвентарем, текст над сердечками, action bar текст, информация на экране, hud, интерфейс, плагин майнкрафт, серверный плагин

**English:** compass, coordinates, direction, biome, radar, locator bar, action bar, death compass, recovery compass, death point, lodestone, navigation, cardinal directions, time of day, world, clock, minecraft time, F3, F3 alternative, action bar text, above inventory text, above hearts text, hud, interface, minecraft plugin, server plugin

</details>

---

## 🔗 Links

<div align="center">

### Plugin (Server)
[![Modrinth](https://img.shields.io/badge/Modrinth-Plugin-00AF5C?style=for-the-badge&logo=modrinth&logoColor=white)](https://modrinth.com/plugin/compasslocator)
[![Hangar](https://img.shields.io/badge/Hangar-Download-1E90FF?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMDAgMTAwIj48cGF0aCBmaWxsPSIjZmZmIiBkPSJNMzAuMSwzMC4xbDE5LjgsMTkuOEwzMC4xLDY5LjdsLTEwLTEwTDUwLDMwLjFsMTAsMTBsLTEwLDEwTDY5LjcsMzAuMXoiLz48L3N2Zz4=)](https://hangar.papermc.io/kasperoid/CompassLocator)
[![CurseForge](https://img.shields.io/badge/CurseForge-Plugin-F16436?style=for-the-badge&logo=curseforge&logoColor=white)](https://www.curseforge.com/minecraft/bukkit-plugins/compasslocator)
[![SpigotMC](https://img.shields.io/badge/SpigotMC-Plugin-ED8106?style=for-the-badge&logo=spigotmc&logoColor=white)](https://www.spigotmc.org/resources/compasslocator.133747/)

### Mod (Client)
[![Modrinth](https://img.shields.io/badge/Modrinth-Mod-00AF5C?style=for-the-badge&logo=modrinth&logoColor=white)](https://modrinth.com/mod/compasslocator-kasperoid)
[![CurseForge](https://img.shields.io/badge/CurseForge-Mod-F16436?style=for-the-badge&logo=curseforge&logoColor=white)](https://www.curseforge.com/minecraft/mc-mods/compasslocator)

### Other
[![GitHub](https://img.shields.io/badge/GitHub-Source-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/kasperoid31/compasslocator)
[![Telegram](https://img.shields.io/badge/Telegram-Channel-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/prostoimpery)

---

<sub>**Version:** 3.6.0 (latest) · **Released:** 17 July 2026 · **Supported:** 1.21-26.2</sub>

© 2026 kasperoid — All Rights Reserved

</div>

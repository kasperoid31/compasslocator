<div align="center">

<img src="https://cdn.modrinth.com/data/cached_images/028c729a257b8817fc93c931f769dab6f3efa248.png" alt="CompassLocator Banner" width="100%">

![Version](https://img.shields.io/badge/version-3.6.0-1E90FF?style=for-the-badge)
![Minecraft](https://img.shields.io/badge/Minecraft-1.21+-4C9A2A?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Paper%20%7C%20Spigot%20%7C%20Purpur-FF6B35?style=for-the-badge)
![Fabric](https://img.shields.io/badge/Fabric-1.21.6+-DBD0B4?style=for-the-badge&logo=fabric&logoColor=black)
![Forge](https://img.shields.io/badge/Forge-1.21.6+-orange?style=for-the-badge)
![Java](https://img.shields.io/badge/Java-21+-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)

[![Modrinth](https://img.shields.io/modrinth/dt/compasslocator?style=for-the-badge&logo=modrinth&logoColor=white&color=00AF5C&label=downloads)](https://modrinth.com/plugin/compasslocator)
[![Telegram](https://img.shields.io/badge/Telegram-channel-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/pro100chnl)

</div>

---

## 📌 What is this?

**CompassLocator** is a plugin **and** client mod that adds useful compass information directly to the action bar.

No more opening F3. Just hold a compass and see:

- where you are
- which direction you're facing
- what biome you're in
- where you died last time

---

## ✨ What does the compass show?

**Normal Compass**
- Coordinates (adjustable precision — integer or decimal)
- Current biome
- Cardinal direction (North/South or N/S — as you prefer)
- Time of day (optional)
- World name (optional)
- If the compass is linked to a lodestone — shows lodestone coordinates

**Recovery Compass**
- Where you last died (coordinates)
- Which world
- Time since death
- Distance to death location

**Combined Mode**
- Hold a normal compass in one hand and a recovery compass in the other
- The action bar shows information from both at once

---

## 📡 Locator Bar (for 1.21.6+)

With a normal compass in hand, you can see other players on the radar (like a minimap). Range is configurable — up to the entire world.

---

## 🖼️ Screenshots

<div align="center">

| Normal Compass | Recovery Compass | Combined Mode | Locator Bar |
|:---:|:---:|:---:|:---:|
| <a href="https://cdn.modrinth.com/data/cached_images/549992fee58de0cbf846a5c41790d109696338b6.png" target="_blank"><img src="https://cdn.modrinth.com/data/cached_images/549992fee58de0cbf846a5c41790d109696338b6.png" width="200"></a> | <a href="https://cdn.modrinth.com/data/cached_images/7109d2b5cb0d9d55bbca0a893bf04ea4fb441116.png" target="_blank"><img src="https://cdn.modrinth.com/data/cached_images/7109d2b5cb0d9d55bbca0a893bf04ea4fb441116.png" width="200"></a> | <a href="https://cdn.modrinth.com/data/cached_images/74b1dc4dbafaf951057f09f72b9edf316fb99d12.png" target="_blank"><img src="https://cdn.modrinth.com/data/cached_images/74b1dc4dbafaf951057f09f72b9edf316fb99d12.png" width="200"></a> | <a href="https://cdn.modrinth.com/data/cached_images/e0602b6da604d308cddcf8ef451dc6cb06271007_0.webp" target="_blank"><img src="https://cdn.modrinth.com/data/cached_images/e0602b6da604d308cddcf8ef451dc6cb06271007_0.webp" width="200"></a> |

</div>

---

## 🎮 For Players

- Works right out of the box — just hold a compass
- Information only appears when you're holding a compass
- Recovery compass shows the way to your items after death
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

## 🔗 Links

<div align="center">

[![Modrinth Plugin](https://img.shields.io/badge/Modrinth-Plugin-00AF5C?style=for-the-badge&logo=modrinth&logoColor=white)](https://modrinth.com/plugin/compasslocator)
[![Modrinth Mod](https://img.shields.io/badge/Modrinth-Mod-00AF5C?style=for-the-badge&logo=modrinth&logoColor=white)](https://modrinth.com/mod/compasslocator-kasperoid)
[![Telegram](https://img.shields.io/badge/Telegram-channel-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/pro100chnl)

---

© 2026 kasperoid — All Rights Reserved

</div>

<p align="center">
  <img src="images/plugin-logo.png" alt="Super Enchantments" width="128" />
</p>
<h1 align="center">Super Enchantments</h1>
<p align="center">
  <b>Extend Minecraft enchanting far beyond vanilla limits.</b><br>
  <b>Levels 1–255 for all vanilla enchantments, plus nine unique custom enchantments.</b>
</p>
<p align="center">
  <a href="https://github.com/Cobbleworks/Super-Enchantments/releases"><img src="https://img.shields.io/github/v/release/Cobbleworks/Super-Enchantments?include_prereleases&style=flat-square&color=4CAF50" alt="Latest Release"></a>&nbsp;&nbsp;<a href="https://github.com/Cobbleworks/Super-Enchantments/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square" alt="License"></a>&nbsp;&nbsp;<img src="https://img.shields.io/badge/Java-17+-orange?style=flat-square" alt="Java Version">&nbsp;&nbsp;<img src="https://img.shields.io/badge/Minecraft-1.21+-green?style=flat-square" alt="Minecraft Version">&nbsp;&nbsp;<img src="https://img.shields.io/badge/Platform-Spigot%2FPaper-yellow?style=flat-square" alt="Platform">&nbsp;&nbsp;<img src="https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square" alt="Status">
</p>

Super Enchantments is an open-source Minecraft plugin that extends the vanilla enchanting system by allowing all standard enchantments to be applied at levels from 1 to 255, far beyond their normal caps. In addition, the plugin introduces nine unique custom enchantments with special abilities, visual effects, and configurable cooldowns — ranging from combat enchantments that fire arrow storms or strike with lightning to utility enchantments that teleport the player forward or summon wolves. All enchantments are applied using a simple command, with context-aware tab completion that suggests only valid enchantments for the item currently held.

### **Core Features**

- **Enhanced Vanilla Enchanting:** Apply any standard Minecraft enchantment at levels 1–255, bypassing traditional level caps
- **Nine Custom Enchantments:** A collection of unique combat and utility enchantments with particle effects, sounds, and cooldown management
- **Smart Item Compatibility:** Automatic compatibility checking ensures only valid enchantments are suggested for the item currently held in hand
- **Context-Aware Tab Completion:** Intelligent tab completion shows only applicable enchantments based on the held item type
- **Configurable Cooldowns:** Built-in cooldown system with optional chat notifications when a custom enchantment is on cooldown
- **Persistent Storage:** Custom enchantments are stored using Minecraft's persistent data container system for reliable cross-restart persistence
- **Visual Feedback:** Particle effects, sounds, and visual indicators play when custom enchantments activate

### **Custom Enchantments**

#### Combat Enchantments
- **Arrow Storm** (Level 1–5): Right-click to fire multiple arrows simultaneously. Higher levels reduce cooldown, tighten spread, and increase arrow count
- **Blazing Shot** (Level 1–5): Launch fireballs that explode on impact. Advanced levels fire multiple projectiles with increased explosion power
- **Venom Strike** (Level 1–5): Chance to poison targets on hit — duration and intensity scale with enchantment level
- **Thunderbolt** (Level 1–5): Chance to strike enemies with lightning — higher levels create multiple simultaneous strikes in a wider area
- **Frostbite** (Level 1–5): Freeze enemies on hit, applying slowness and mining fatigue that scale with enchantment level
- **Soul Drain** (Level 1–5): Life-steal enchantment that heals the player for a portion of damage dealt — healing scales with level

#### Utility Enchantments
- **Void Step** (Level 1–3): Teleport forward through obstacles and terrain — higher levels increase distance and reduce cooldown
- **Pack Leader** (Level 1–3): Summon tamed wolves to fight for you — level determines wolf count, duration, and combat effectiveness

### **Enchantment Compatibility**

| Category | Applicable Items |
|----------|-----------------|
| Weapon enchantments | Swords, axes, tridents, and themed utility items |
| Tool enchantments | All standard tools plus special items such as sticks |
| Ranged enchantments | Bows and crossbows for projectile-based abilities |
| Special items | Custom enchantments can be applied to themed items (e.g., bones for Pack Leader, ender pearls for Void Step) |

### **Supported Platforms**

- **Server Software:** `Spigot`, `Paper`, `Purpur`, `CraftBukkit`
- **Minecraft Versions:** `1.21.5`, `1.21.6`, `1.21.7`, `1.21.8`, `1.21.9`, `1.21.10` and higher
- **Java Requirements:** `Java 17+`

### **Installation**

1. Download the latest `.jar` from the [Releases](https://github.com/Cobbleworks/Super-Enchantments/releases) page
2. Stop your Minecraft server
3. Copy the `.jar` into your server's `plugins` folder
4. Start your server — a default configuration folder is generated at `plugins/SuperEnchantments/`

### **Player Commands**

| Command | Permission | Description |
|---------|-----------|-------------|
| `/superenchant <enchantment> [level]` | `superenchantments.use` | Apply a vanilla enchantment at levels 1–255 to the held item |
| `/superenchant customs <enchantment> [level]` | `superenchantments.use` | Apply a custom enchantment to the held item |
| `/enchantlist` | `superenchantments.list` | Show all applicable enchantments for the item currently held in hand |
| `/superenchant togglecooldown` | `superenchantments.admin` | Toggle cooldown notification messages on or off |

**Aliases:** `/senchant`, `/se` for `/superenchant` | `/elist`, `/el` for `/enchantlist`

**Default Permissions:** `superenchantments.list` is enabled for all players by default. `superenchantments.use` requires operator access by default.

### **Usage Examples**

```
/superenchant sharpness 100           — Apply Sharpness 100 to the held weapon
/superenchant customs arrow_storm 3   — Apply Arrow Storm level 3 to the held item
/superenchant efficiency 255          — Apply maximum Efficiency to the held tool
/enchantlist                          — Show which enchantments can be applied to the held item
```

### **License**

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.


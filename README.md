<p align="center">
  <img src="images/ <p align="center">
  <img src="images/plugin-logo.png" alt="Super Enchantments" width="180" />
</p>
<h1 align="center">Super Enchantments</h1>
<p align="center">
  <b>Extend Minecraft enchanting far beyond vanilla limits.</b><br>
  <b>Levels 1â€“255 for all vanilla enchantments, plus nine unique custom enchantments.</b>
</p>
<p align="center">
  <a href="https://github.com/Cobbleworks/Super-Enchantments/releases"><img src="https://img.shields.io/github/v/release/Cobbleworks/Super-Enchantments?include_prereleases&style=flat-square&color=4CAF50" alt="Latest Release"></a>&nbsp;&nbsp;<a href="https://github.com/Cobbleworks/Super-Enchantments/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square" alt="License"></a>&nbsp;&nbsp;<img src="https://img.shields.io/badge/Java-17+-orange?style=flat-square" alt="Java Version">&nbsp;&nbsp;<img src="https://img.shields.io/badge/Minecraft-1.21+-green?style=flat-square" alt="Minecraft Version">&nbsp;&nbsp;<img src="https://img.shields.io/badge/Platform-Spigot%2FPaper-yellow?style=flat-square" alt="Platform">&nbsp;&nbsp;<img src="https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square" alt="Status">
</p>

Super Enchantments is an open-source Minecraft plugin that extends the vanilla enchanting system by allowing all standard enchantments to be applied at levels from 1 to 255, far beyond their normal caps. In addition, the plugin introduces nine unique custom enchantments with special abilities, visual effects, and configurable cooldowns â€” ranging from combat enchantments that fire arrow storms or strike with lightning to utility enchantments that teleport the player forward or summon wolves. All enchantments are applied using a simple command, with context-aware tab completion that suggests only valid enchantments for the item currently held.

### **Core Features**

- **Enhanced Vanilla Enchanting:** Apply vanilla enchantments at levels `1..255` (`unsafe` application enabled)
- **Nine Custom Enchantments:** Custom combat/utility enchantments with trigger events, particles, sounds, and per-player cooldown behavior
- **Smart Item Compatibility:** Automatic compatibility checking ensures only valid enchantments are suggested for the item currently held in hand
- **Context-Aware Tab Completion:** Intelligent tab completion shows only applicable enchantments based on the held item type
- **Configurable Cooldowns:** Built-in cooldown system with optional chat notifications when a custom enchantment is on cooldown
- **Persistent Storage:** Custom enchantments are stored using Minecraft's persistent data container system for reliable cross-restart persistence
- **Visual Feedback:** Particle effects, sounds, and visual indicators play when custom enchantments activate

### **Custom Enchantments**

| Enchantment | Max Level | Trigger | Can Apply To |
|-------------|-----------|---------|--------------|
| `arrow_storm` | `5` | Right-click (`PlayerInteractEvent`) | swords, axes, pickaxes, shovels, hoes, stick |
| `blazing_shot` | `5` | Right-click (`PlayerInteractEvent`) | swords, axes, pickaxes, shovels, hoes, stick, blaze rod |
| `venom_strike` | `5` | Melee hit (`EntityDamageByEntityEvent`) | swords, axes, stick, spider eye items |
| `thunderbolt` | `5` | Melee hit (`EntityDamageByEntityEvent`) | swords, axes, trident, stick |
| `frostbite` | `5` | Melee hit (`EntityDamageByEntityEvent`) | swords, axes, trident, ice variants |
| `soul_drain` | `5` | Melee hit (`EntityDamageByEntityEvent`) | swords, axes, stick |
| `void_step` | `3` | Right-click (`PlayerInteractEvent`) | ender pearl, chorus fruit, stick, swords, axes |
| `explosive_tip` | `4` | Bow shot/hit events | bow, crossbow |
| `pack_leader` | `3` | Right-click (`PlayerInteractEvent`) | bone, stick, swords, axes |

### **Enchantment Compatibility**

| Category | Applicable Items |
|----------|-----------------|
| Weapon enchantments | Swords, axes, tridents, and themed utility items |
| Tool enchantments | All standard tools plus special items such as sticks |
| Ranged enchantments | Bows and crossbows for projectile-based abilities |
| Special items | Custom enchantments can be applied to themed items (e.g., bones for Pack Leader, ender pearls for Void Step) |

### **Supported Platforms**

- **Server Software:** `Spigot`, `Paper`, `Purpur`, `CraftBukkit`
- **Minecraft Versions:** `1.13` and higher
- **Java Requirements:** `Java 17+`

### **Installation**

1. Download the latest `.jar` from the [Releases](https://github.com/Cobbleworks/Super-Enchantments/releases) page
2. Stop your Minecraft server
3. Copy the `.jar` into your server's `plugins/` folder
4. Start your server â€” a default configuration folder is generated at `plugins/SuperEnchantments/`

### **Player Commands**

| Command | Permission | Description |
|---------|-----------|-------------|
| `/superenchant <enchantment> [level]` | `superenchantments.use` | Apply a vanilla enchantment to held item (`level` default = configured vanilla max map) |
| `/superenchant customs <enchantment> [level]` | `superenchantments.use` | Apply a custom enchantment to held item (`level` default = custom enchant max) |
| `/enchantlist` | `superenchantments.list` | Show all applicable enchantments for the item currently held in hand |
| `/superenchant togglecooldown` | `superenchant.admin` | Toggle cooldown notification messages on or off |

**Aliases:** `/senchant`, `/se` for `/superenchant` | `/elist`, `/el` for `/enchantlist`

**Default Permissions:** `superenchantments.list` is enabled for all players by default. `superenchantments.use` requires operator access by default.

### **Configuration**

All settings are in `plugins/SuperEnchantments/config.yml`.

| Key | Default | Description |
|-----|---------|-------------|
| `cooldown-display-enabled` | `true` | Show cooldown messages when abilities are still on cooldown |
| `arrowstorm.cooldown-base` | `6` | Base cooldown in seconds |
| `arrowstorm.cooldown-reduction` | `1` | Cooldown reduction per level |
| `arrowstorm.arrow-count-base` | `1` | Base arrow count |
| `arrowstorm.arrow-count-increase` | `1` | Additional arrows per level |
| `arrowstorm.speed-base` | `1.5` | Base arrow speed |
| `arrowstorm.speed-increase` | `0.3` | Arrow speed increase per level |
| `arrowstorm.damage-base` | `2.0` | Base arrow damage |
| `arrowstorm.damage-increase` | `0.8` | Arrow damage increase per level |
| `arrowstorm.spread-base` | `0.1` | Base spread |
| `arrowstorm.spread-reduction` | `0.05` | Spread reduction per level |
| `blazingshot.cooldown-base` | `8` | Base cooldown in seconds |
| `blazingshot.cooldown-reduction` | `2` | Cooldown reduction per level |
| `blazingshot.fireball-count-base` | `1` | Base fireball count |
| `blazingshot.fireball-count-increase` | `1` | Additional fireballs scaling |
| `blazingshot.yield-base` | `0.5` | Base explosion yield |
| `blazingshot.yield-increase` | `0.4` | Explosion yield increase per level |
| `blazingshot.velocity-base` | `1.2` | Base projectile velocity multiplier |
| `blazingshot.velocity-increase` | `0.15` | Velocity increase per level |
| `blazingshot.spread-base` | `0.2` | Base projectile spread |
| `blazingshot.spread-reduction` | `0.05` | Spread adjustment per level |
| `voidstep.cooldown-base` | `10` | Base cooldown in seconds |
| `voidstep.cooldown-reduction` | `2` | Cooldown reduction per level |
| `voidstep.distance-base` | `5` | Base teleport distance |
| `voidstep.distance-increase` | `5` | Extra teleport distance per level |
| `packleader.cooldown-base` | `15` | Base cooldown in seconds |
| `packleader.cooldown-reduction` | `3` | Cooldown reduction per level |
| `packleader.wolf-count-base` | `1` | Base wolf count |
| `packleader.wolf-count-increase` | `1` | Additional wolves per level |
| `explosivetip.power-base` | `0.5` | Base explosion power |
| `explosivetip.power-increase` | `0.8` | Explosion power increase per level |
| `frostbite.chance-base` | `0.10` | Base trigger chance |
| `frostbite.chance-increase` | `0.08` | Chance increase per level |
| `frostbite.duration-base` | `1.5` | Base effect duration in seconds |
| `frostbite.duration-increase` | `0.5` | Duration increase per level |
| `frostbite.intensity-base` | `1` | Base slowness intensity |
| `frostbite.intensity-increase` | `1` | Intensity increase per level |
| `thunderbolt.chance-base` | `0.05` | Base trigger chance |
| `thunderbolt.chance-increase` | `0.03` | Chance increase per level |
| `thunderbolt.strike-count-base` | `1` | Base strike count |
| `thunderbolt.strike-count-increase` | `0.5` | Strike count increase per level |
| `thunderbolt.spread-radius` | `3.0` | Lightning spread radius |
| `venom_strike.chance-base` | `0.10` | Base trigger chance |
| `venom_strike.chance-increase` | `0.05` | Chance increase per level |
| `venom_strike.duration-base` | `3.0` | Base poison duration in seconds |
| `venom_strike.duration-increase` | `1.0` | Poison duration increase per level |
| `venom_strike.intensity-base` | `0` | Base poison amplifier |
| `venom_strike.intensity-increase` | `1` | Poison amplifier increase per level |
| `soul_drain.chance-base` | `0.15` | Base trigger chance |
| `soul_drain.chance-increase` | `0.10` | Chance increase per level |
| `soul_drain.healing-multiplier-base` | `0.20` | Base healing multiplier |
| `soul_drain.healing-multiplier-increase` | `0.10` | Healing multiplier increase per level |
| `soul_drain.particle-count-base` | `3` | Base heart particle count |
| `soul_drain.particle-count-increase` | `2` | Extra particles per level |

### **Permissions**

| Permission | Description | Default |
|------------|-------------|---------|
| `superenchantments.use` | Allows using super enchantments and custom enchantments | `op` |
| `superenchantments.list` | Allows viewing available enchantments | `true` |

**Note:** `/superenchant togglecooldown` checks for `superenchant.admin` in command logic, which is not declared in `plugin.yml`.

### **Usage Examples**

```
/superenchant sharpness 100           â€” Apply Sharpness 100 to the held weapon
/superenchant customs arrow_storm 3   â€” Apply Arrow Storm level 3 to the held item
/superenchant efficiency 255          â€” Apply maximum Efficiency to the held tool
/enchantlist                          â€” Show which enchantments can be applied to the held item
```

### **License**

This project is licensed under the **MIT License** â€” see the [LICENSE](LICENSE) file for details.


## **Screenshots**

The screenshots below demonstrate the core features of the Super Enchantments plugin, including a level 255 Unbreaking enchantment and the wolf summoning combat ability.

<table>
  <tr>
    <th>Super Enchantments - Level 255 Unbreaking</th>
    <th>Super Enchantments - Wolf Summoning</th>
  </tr>
  <tr>
    <td><a href="https://github.com/Cobbleworks/Super-Enchantments/raw/main/images/screenshot-enchantment-255.png" target="_blank" rel="noopener noreferrer"><img src="https://github.com/Cobbleworks/Super-Enchantments/raw/main/images/screenshot-enchantment-255.png" alt="Level 255 Unbreaking" width="450"></a></td>
    <td><a href="https://github.com/Cobbleworks/Super-Enchantments/raw/main/images/screenshot-wolf-summon.png" target="_blank" rel="noopener noreferrer"><img src="https://github.com/Cobbleworks/Super-Enchantments/raw/main/images/screenshot-wolf-summon.png" alt="Wolf Summoning" width="450"></a></td>
  </tr>
</table>
.Value -replace 'width="180"', 'width="180"'  />
</p>
<h1 align="center">Super Enchantments</h1>
<p align="center">
  <b>Extend Minecraft enchanting far beyond vanilla limits.</b><br>
  <b>Levels 1â€“255 for all vanilla enchantments, plus nine unique custom enchantments.</b>
</p>
<p align="center">
  <a href="https://github.com/Cobbleworks/Super-Enchantments/releases"><img src="https://img.shields.io/github/v/release/Cobbleworks/Super-Enchantments?include_prereleases&style=flat-square&color=4CAF50" alt="Latest Release"></a>&nbsp;&nbsp;<a href="https://github.com/Cobbleworks/Super-Enchantments/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square" alt="License"></a>&nbsp;&nbsp;<img src="https://img.shields.io/badge/Java-17+-orange?style=flat-square" alt="Java Version">&nbsp;&nbsp;<img src="https://img.shields.io/badge/Minecraft-1.21+-green?style=flat-square" alt="Minecraft Version">&nbsp;&nbsp;<img src="https://img.shields.io/badge/Platform-Spigot%2FPaper-yellow?style=flat-square" alt="Platform">&nbsp;&nbsp;<img src="https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square" alt="Status">
</p>

Super Enchantments is an open-source Minecraft plugin that extends the vanilla enchanting system by allowing all standard enchantments to be applied at levels from 1 to 255, far beyond their normal caps. In addition, the plugin introduces nine unique custom enchantments with special abilities, visual effects, and configurable cooldowns â€” ranging from combat enchantments that fire arrow storms or strike with lightning to utility enchantments that teleport the player forward or summon wolves. All enchantments are applied using a simple command, with context-aware tab completion that suggests only valid enchantments for the item currently held.

### **Core Features**

- **Enhanced Vanilla Enchanting:** Apply vanilla enchantments at levels `1..255` (`unsafe` application enabled)
- **Nine Custom Enchantments:** Custom combat/utility enchantments with trigger events, particles, sounds, and per-player cooldown behavior
- **Smart Item Compatibility:** Automatic compatibility checking ensures only valid enchantments are suggested for the item currently held in hand
- **Context-Aware Tab Completion:** Intelligent tab completion shows only applicable enchantments based on the held item type
- **Configurable Cooldowns:** Built-in cooldown system with optional chat notifications when a custom enchantment is on cooldown
- **Persistent Storage:** Custom enchantments are stored using Minecraft's persistent data container system for reliable cross-restart persistence
- **Visual Feedback:** Particle effects, sounds, and visual indicators play when custom enchantments activate

### **Custom Enchantments**

| Enchantment | Max Level | Trigger | Can Apply To |
|-------------|-----------|---------|--------------|
| `arrow_storm` | `5` | Right-click (`PlayerInteractEvent`) | swords, axes, pickaxes, shovels, hoes, stick |
| `blazing_shot` | `5` | Right-click (`PlayerInteractEvent`) | swords, axes, pickaxes, shovels, hoes, stick, blaze rod |
| `venom_strike` | `5` | Melee hit (`EntityDamageByEntityEvent`) | swords, axes, stick, spider eye items |
| `thunderbolt` | `5` | Melee hit (`EntityDamageByEntityEvent`) | swords, axes, trident, stick |
| `frostbite` | `5` | Melee hit (`EntityDamageByEntityEvent`) | swords, axes, trident, ice variants |
| `soul_drain` | `5` | Melee hit (`EntityDamageByEntityEvent`) | swords, axes, stick |
| `void_step` | `3` | Right-click (`PlayerInteractEvent`) | ender pearl, chorus fruit, stick, swords, axes |
| `explosive_tip` | `4` | Bow shot/hit events | bow, crossbow |
| `pack_leader` | `3` | Right-click (`PlayerInteractEvent`) | bone, stick, swords, axes |

### **Enchantment Compatibility**

| Category | Applicable Items |
|----------|-----------------|
| Weapon enchantments | Swords, axes, tridents, and themed utility items |
| Tool enchantments | All standard tools plus special items such as sticks |
| Ranged enchantments | Bows and crossbows for projectile-based abilities |
| Special items | Custom enchantments can be applied to themed items (e.g., bones for Pack Leader, ender pearls for Void Step) |

### **Supported Platforms**

- **Server Software:** `Spigot`, `Paper`, `Purpur`, `CraftBukkit`
- **Minecraft Versions:** `1.13` and higher
- **Java Requirements:** `Java 17+`

### **Installation**

1. Download the latest `.jar` from the [Releases](https://github.com/Cobbleworks/Super-Enchantments/releases) page
2. Stop your Minecraft server
3. Copy the `.jar` into your server's `plugins/` folder
4. Start your server â€” a default configuration folder is generated at `plugins/SuperEnchantments/`

### **Player Commands**

| Command | Permission | Description |
|---------|-----------|-------------|
| `/superenchant <enchantment> [level]` | `superenchantments.use` | Apply a vanilla enchantment to held item (`level` default = configured vanilla max map) |
| `/superenchant customs <enchantment> [level]` | `superenchantments.use` | Apply a custom enchantment to held item (`level` default = custom enchant max) |
| `/enchantlist` | `superenchantments.list` | Show all applicable enchantments for the item currently held in hand |
| `/superenchant togglecooldown` | `superenchant.admin` | Toggle cooldown notification messages on or off |

**Aliases:** `/senchant`, `/se` for `/superenchant` | `/elist`, `/el` for `/enchantlist`

**Default Permissions:** `superenchantments.list` is enabled for all players by default. `superenchantments.use` requires operator access by default.

### **Configuration**

All settings are in `plugins/SuperEnchantments/config.yml`.

| Key | Default | Description |
|-----|---------|-------------|
| `cooldown-display-enabled` | `true` | Show cooldown messages when abilities are still on cooldown |
| `arrowstorm.cooldown-base` | `6` | Base cooldown in seconds |
| `arrowstorm.cooldown-reduction` | `1` | Cooldown reduction per level |
| `arrowstorm.arrow-count-base` | `1` | Base arrow count |
| `arrowstorm.arrow-count-increase` | `1` | Additional arrows per level |
| `arrowstorm.speed-base` | `1.5` | Base arrow speed |
| `arrowstorm.speed-increase` | `0.3` | Arrow speed increase per level |
| `arrowstorm.damage-base` | `2.0` | Base arrow damage |
| `arrowstorm.damage-increase` | `0.8` | Arrow damage increase per level |
| `arrowstorm.spread-base` | `0.1` | Base spread |
| `arrowstorm.spread-reduction` | `0.05` | Spread reduction per level |
| `blazingshot.cooldown-base` | `8` | Base cooldown in seconds |
| `blazingshot.cooldown-reduction` | `2` | Cooldown reduction per level |
| `blazingshot.fireball-count-base` | `1` | Base fireball count |
| `blazingshot.fireball-count-increase` | `1` | Additional fireballs scaling |
| `blazingshot.yield-base` | `0.5` | Base explosion yield |
| `blazingshot.yield-increase` | `0.4` | Explosion yield increase per level |
| `blazingshot.velocity-base` | `1.2` | Base projectile velocity multiplier |
| `blazingshot.velocity-increase` | `0.15` | Velocity increase per level |
| `blazingshot.spread-base` | `0.2` | Base projectile spread |
| `blazingshot.spread-reduction` | `0.05` | Spread adjustment per level |
| `voidstep.cooldown-base` | `10` | Base cooldown in seconds |
| `voidstep.cooldown-reduction` | `2` | Cooldown reduction per level |
| `voidstep.distance-base` | `5` | Base teleport distance |
| `voidstep.distance-increase` | `5` | Extra teleport distance per level |
| `packleader.cooldown-base` | `15` | Base cooldown in seconds |
| `packleader.cooldown-reduction` | `3` | Cooldown reduction per level |
| `packleader.wolf-count-base` | `1` | Base wolf count |
| `packleader.wolf-count-increase` | `1` | Additional wolves per level |
| `explosivetip.power-base` | `0.5` | Base explosion power |
| `explosivetip.power-increase` | `0.8` | Explosion power increase per level |
| `frostbite.chance-base` | `0.10` | Base trigger chance |
| `frostbite.chance-increase` | `0.08` | Chance increase per level |
| `frostbite.duration-base` | `1.5` | Base effect duration in seconds |
| `frostbite.duration-increase` | `0.5` | Duration increase per level |
| `frostbite.intensity-base` | `1` | Base slowness intensity |
| `frostbite.intensity-increase` | `1` | Intensity increase per level |
| `thunderbolt.chance-base` | `0.05` | Base trigger chance |
| `thunderbolt.chance-increase` | `0.03` | Chance increase per level |
| `thunderbolt.strike-count-base` | `1` | Base strike count |
| `thunderbolt.strike-count-increase` | `0.5` | Strike count increase per level |
| `thunderbolt.spread-radius` | `3.0` | Lightning spread radius |
| `venom_strike.chance-base` | `0.10` | Base trigger chance |
| `venom_strike.chance-increase` | `0.05` | Chance increase per level |
| `venom_strike.duration-base` | `3.0` | Base poison duration in seconds |
| `venom_strike.duration-increase` | `1.0` | Poison duration increase per level |
| `venom_strike.intensity-base` | `0` | Base poison amplifier |
| `venom_strike.intensity-increase` | `1` | Poison amplifier increase per level |
| `soul_drain.chance-base` | `0.15` | Base trigger chance |
| `soul_drain.chance-increase` | `0.10` | Chance increase per level |
| `soul_drain.healing-multiplier-base` | `0.20` | Base healing multiplier |
| `soul_drain.healing-multiplier-increase` | `0.10` | Healing multiplier increase per level |
| `soul_drain.particle-count-base` | `3` | Base heart particle count |
| `soul_drain.particle-count-increase` | `2` | Extra particles per level |

### **Permissions**

| Permission | Description | Default |
|------------|-------------|---------|
| `superenchantments.use` | Allows using super enchantments and custom enchantments | `op` |
| `superenchantments.list` | Allows viewing available enchantments | `true` |

**Note:** `/superenchant togglecooldown` checks for `superenchant.admin` in command logic, which is not declared in `plugin.yml`.

### **Usage Examples**

```
/superenchant sharpness 100           â€” Apply Sharpness 100 to the held weapon
/superenchant customs arrow_storm 3   â€” Apply Arrow Storm level 3 to the held item
/superenchant efficiency 255          â€” Apply maximum Efficiency to the held tool
/enchantlist                          â€” Show which enchantments can be applied to the held item
```

### **License**

This project is licensed under the **MIT License** â€” see the [LICENSE](LICENSE) file for details.


## **Screenshots**

The screenshots below demonstrate the core features of the Super Enchantments plugin, including a level 255 Unbreaking enchantment and the wolf summoning combat ability.

<table>
  <tr>
    <th>Super Enchantments - Level 255 Unbreaking</th>
    <th>Super Enchantments - Wolf Summoning</th>
  </tr>
  <tr>
    <td><a href="https://github.com/Cobbleworks/Super-Enchantments/raw/main/images/screenshot-enchantment-255.png" target="_blank" rel="noopener noreferrer"><img src="https://github.com/Cobbleworks/Super-Enchantments/raw/main/images/screenshot-enchantment-255.png" alt="Level 255 Unbreaking" width="450"></a></td>
    <td><a href="https://github.com/Cobbleworks/Super-Enchantments/raw/main/images/screenshot-wolf-summon.png" target="_blank" rel="noopener noreferrer"><img src="https://github.com/Cobbleworks/Super-Enchantments/raw/main/images/screenshot-wolf-summon.png" alt="Wolf Summoning" width="450"></a></td>
  </tr>
</table>

# Super Enchantments

Part of the Cobbleworks Minecraft plugin ecosystem.

Source section copied from the main plugin collection repository:
https://github.com/BerndHagen/Minecraft-Server-Plugins

## Overview

A comprehensive enchantment system that extends vanilla Minecraft enchanting capabilities by allowing all vanilla enchantments with levels 1-255, plus a collection of powerful custom enchantments with unique abilities. Each enchantment is carefully balanced with configurable cooldowns, effects, and compatibility checks.

### Core Features:
- **Enhanced Vanilla Enchanting:** Apply any vanilla enchantment with levels 1-255, breaking traditional level limits
- **Custom Enchantments:** 9 unique custom enchantments with special abilities and visual effects
- **Smart Compatibility:** Automatic item compatibility checking - only valid enchantments are suggested
- **Intelligent Tab Completion:** Context-aware suggestions showing only applicable enchantments for held items
- **Configurable System:** Extensive configuration options for cooldowns, damage, effects, and behavior
- **Cooldown Management:** Built-in cooldown system with optional display messages for custom enchantments
- **Persistent Storage:** Custom enchantments are stored using Minecraft's persistent data containers
- **Visual Feedback:** Particle effects, sounds, and visual indicators for enchantment activation

### Custom Enchantments:

#### **Combat Enchantments**
- **Arrow Storm** (Level 1-5): Right-click to fire multiple arrows with increased damage and speed. Higher levels reduce cooldown and spread while increasing arrow count
- **Blazing Shot** (Level 1-5): Launch fireballs that explode on impact. Advanced levels fire multiple projectiles with increased explosion power
- **Venom Strike** (Level 1-5): Chance to poison targets on hit with increasing duration and intensity based on enchantment level
- **Thunderbolt** (Level 1-5): Chance to strike enemies with lightning, with higher levels creating multiple strikes in a wider area
- **Frostbite** (Level 1-5): Freeze enemies on hit, applying slowness and mining fatigue effects that scale with level
- **Soul Drain** (Level 1-5): Life-steal enchantment that heals the player based on damage dealt, with healing scaling by level

#### **Utility Enchantments**
- **Void Step** (Level 1-3): Teleport forward through obstacles and terrain. Higher levels increase teleport distance and reduce cooldown
- **Pack Leader** (Level 1-3): Summon tamed wolves to fight alongside you. Level determines wolf count, duration, and combat effectiveness

### Enchantment Compatibility:
- **Weapon Enchantments:** Swords, axes, tridents, and some utility items
- **Tool Enchantments:** All vanilla tools plus special items like sticks and rods
- **Ranged Enchantments:** Bows, crossbows for projectile-based abilities
- **Special Items:** Custom enchantments can be applied to themed items (e.g., bones for Pack Leader, ender pearls for Void Step)

### Player Commands:
| Command | Description | Permission |
|---------|-------------|------------|
| `/superenchant <enchantment> [level]` | Apply vanilla enchantment (1-255) | `superenchantments.use` |
| `/superenchant customs <enchantment> [level]` | Apply custom enchantment | `superenchantments.use` |
| `/enchantlist` | Show available enchantments for held item | `superenchantments.list` |
| `/superenchant togglecooldown` | Toggle cooldown display messages (admin) | `superenchantments.admin` |

### Usage Examples:
```
/superenchant sharpness 100          # Apply Sharpness 100 to held weapon
/superenchant customs arrow_storm 3   # Apply Arrow Storm level 3
/superenchant efficiency 255          # Maximum vanilla efficiency
/enchantlist                         # See what can be enchanted
```

**Aliases:** `/senchant`, `/se` for `/superenchant` | `/elist`, `/el` for `/enchantlist`  
**Requirements:** Item must be held in main hand and be enchantable  
**Permissions:** Default permissions allow listing (`superenchantments.list: true`) but restrict usage to operators (`superenchantments.use: op`)

**Note:** Custom enchantments use a sophisticated trigger system that responds to different events (combat, interaction, projectile hits) and include built-in cooldowns to maintain game balance. All effects are configurable through the plugin's config.yml file.

## License

This project is licensed under the MIT License.
# Changelog

All notable changes to Super Enchantments will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [Unreleased]

## [1.0.2] - 2026-04-28

Super Enchantments v1.0.2 delivers stability improvements and maintenance fixes following the initial release.

### Stability And Maintenance

- **Runtime Safety**: Improved error handling around enchantment activation and cooldown tracking
- **General Refinements**: Applied maintenance updates for long-running servers

**Note:** If you encounter any bugs or issues, please don't hesitate to open an [issue](https://github.com/Cobbleworks/Super-Enchantments-Plugin/issues). For any questions or to start a discussion, feel free to initiate a [discussion](https://github.com/Cobbleworks/Super-Enchantments-Plugin/discussions) on the GitHub repository.

## [1.0.0] - 2026-04-01

Super Enchantments v1.0.0 is the initial release, extending vanilla enchanting to level 255 and adding nine custom enchantments with combat and utility abilities, visual effects, and per-player cooldowns.

### Enhanced Vanilla Enchanting

- **Level 1–255 Support**: All standard vanilla enchantments can be applied far beyond their normal caps using unsafe application
- **Smart Item Compatibility**: Only enchantments valid for the currently held item type are suggested
- **Context-Aware Tab Completion**: Tab completion is filtered by the held item to prevent invalid applications

### Custom Enchantments

- **Nine Unique Enchantments**: Custom combat and utility enchantments with trigger events, particle effects, sounds, and special abilities
- **Per-Player Cooldowns**: Built-in cooldown system with optional chat notification when a custom enchantment is on cooldown
- **Visual Feedback**: Particle effects, sounds, and visual indicators play when custom enchantments activate

### Persistence

- **Persistent Data Container**: Custom enchantment state stored using Minecraft's built-in persistent data container for reliable cross-restart persistence

**Note:** If you encounter any bugs or issues, please don't hesitate to open an [issue](https://github.com/Cobbleworks/Super-Enchantments-Plugin/issues). For any questions or to start a discussion, feel free to initiate a [discussion](https://github.com/Cobbleworks/Super-Enchantments-Plugin/discussions) on the GitHub repository.

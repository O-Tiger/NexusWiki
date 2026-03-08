# NexusSlime

> **A comprehensive reimplementation and evolution of Slimefun4** — next-generation tech, magic, and quality-of-life systems for Minecraft servers.

NexusSlime is a modular Spigot plugin built on a 27-module Maven architecture. It brings custom items, machines, energy networks, clans, economy, minigames, and deep integrations all under a single, lightweight plugin JAR.

---

## Key Features

| Category | Highlights |
| --- | --- |
| **Custom Items** | 235+ data-driven items defined in YAML |
| **Machines** | Multiblock crafting, energy networks, ME storage |
| **Economy** | Dual-currency (money + credits), /sell, /baltop |
| **Clans** | Territory claiming, upgrades, clan chest, clan chat |
| **Essentials** | 40+ QoL commands — homes, warps, TPA, AFK, jail |
| **Security** | BCrypt auth, CAPTCHA anti-bot, anti-dupe, anti-lag |
| **Discord** | Bot integration, account linking, role sync |
| **Crystal Defense** | Wave-based minigame protecting Ender Crystals |
| **Custom Mobs** | YAML-defined bosses with loot tables and AI forms |
| **Votifier** | Standalone V1/V2 vote server, streaks, leaderboards |
| **Dreams** | Sleep cutscene system with nightmare variants |
| **Protections** | Region claims, flags, duel arena system |
| **Twitch** | Account linking, live alerts, chat relay, giveaways |
| **PlaceholderAPI** | 30+ placeholders across all modules |

---

## Module Overview

```c#
NexusSlime
├── nexusslime-api          Public API for addon developers
├── nexusslime-core         Core managers, PDC registry, language
├── nexusslime-items        Custom item storage (235+ items)
├── nexusslime-machines     Machine definitions, processing engine
├── nexusslime-systems      Energy network implementation
├── nexusslime-integrations PlaceholderAPI, LuckPerms, SkinsRestorer
├── nexusslime-storage      SQLite / PostgreSQL persistence
├── nexusslime-gui          GUI framework
├── nexusslime-utils        Utility helpers
├── nexusslime-web          Webstore delivery, VIP kits, payments
├── nexusslime-plugin       Main entry point (Spigot)
├── nexusslime-discord      JDA bot, webhooks, account linking
├── nexusslime-chat         4-channel chat system
├── nexusslime-ae           ME (Applied Energistics-style) storage
├── nexusslime-energy       Energy generation and cable networks
├── nexusslime-waila        WAILA/HUD integration
├── nexusslime-security     Auth, anti-bot, anti-lag, anti-dupe
├── nexusslime-clans        Clans, territory, upgrades
├── nexusslime-economy      Money, credits, sell prices
├── nexusslime-essentials   40+ QoL commands
├── nexusslime-crystaldefense Wave-based Crystal Defense minigame
├── nexusslime-custommobs   YAML-defined bosses
├── nexusslime-dreams       Sleep cutscene system
├── nexusslime-protections  Region protection, duel system
├── nexusslime-ss           Silk Spawner support
├── nexusslime-votifier     Standalone Votifier V1/V2 server
└── nexusslime-twitch       Twitch integration
```

---

## Quick Navigation

- :material-rocket-launch: **[Getting Started](getting-started.md)**
  Installation, requirements, and first steps

- :material-cog: **[Core Module](modules/core.md)**
  Items, PDC system, custom item registry

- :material-sword: **[All Modules](modules/index.md)**
  Browse all 13 feature modules

- :material-console: **[Commands Reference](reference/commands.md)**
  All 40+ commands with usage and permissions

- :material-key: **[Permissions Reference](reference/permissions.md)**
  Complete permission node list

- :material-format-list-text: **[PlaceholderAPI](reference/placeholders.md)**
  All `%nexusslime_*%` placeholders

</div>

---

## Authors

NexusSlime is developed by **O-Tiger**, **8-byte**, and **HexNode**.

- API version: `1.21`
- Soft dependencies: `PlaceholderAPI`, `LuckPerms`, `SkinsRestorer`

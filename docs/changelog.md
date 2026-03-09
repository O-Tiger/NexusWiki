# Changelog

All notable changes to NexusSlime are documented here. NexusSlime follows [Semantic Versioning](https://semver.org/).

---

## [2.0.0-BETA] — Current

### Architecture

- Complete rewrite as a **27-module Maven multi-module project**
- New `nexusslime-api` module providing a public API for addon developers
- All feature systems are now self-contained modules with their own lifecycle
- Switched from YAML-only persistence to **SQLite / PostgreSQL** via `nexusslime-storage`

### Core

- `CustomItemRegistry` with PDC-based item tagging (`nexusslime:id`)
- 235+ data-driven items defined in `items.yml`
- Item tier system: Basic → Advanced → Infinity
- Research tree with XP-gated unlocks
- Multi-language support: English, Brazilian Portuguese, Spanish, Simplified Chinese

### Modules Added

- **nexusslime-essentials** — 40+ QoL commands (homes, warps, TPA, AFK, jail, utility)
- **nexusslime-economy** — Dual-currency system, `/sell`, `/baltop`, configurable sell prices
- **nexusslime-clans** — Territory claiming, upgrade tree, clan chest, clan chat
- **nexusslime-security** — BCrypt auth, CAPTCHA anti-bot, VPN detection, anti-lag, anti-dupe
- **nexusslime-discord** — JDA bot, account linking, role sync, webhooks, GitHub Actions monitoring
- **nexusslime-crystaldefense** — Wave-based cooperative minigame
- **nexusslime-votifier** — Standalone Votifier V1/V2 server with streaks and leaderboard
- **nexusslime-dreams** — Sleep cutscene system (dreams and nightmares)
- **nexusslime-protections** — Region claiming, flags, 1v1 duel system
- **nexusslime-custommobs** — YAML-defined bosses with AI forms and loot tables
- **nexusslime-twitch** — Account linking, live alerts, chat relay, viewer giveaways
- **nexusslime-ae** — ME (Applied Energistics-style) network storage
- **nexusslime-energy** — Energy generation and cable networks
- **nexusslime-chat** — 4-channel chat (global, local, staff, trade) with moderation
- **nexusslime-waila** — WAILA/HUD machine tooltips
- **nexusslime-ss** — Silk Spawner support
- **nexusslime-web** — Webstore delivery bridge, VIP kits, payment handling, GDPR

### Integrations

- **PlaceholderAPI** — 14 providers, 30+ placeholders across all modules
- **LuckPerms** — Permissions and group-based placeholders
- **SkinsRestorer** — Skin management for cracked servers

### Machines

- `MachineYamlLoader` — machines defined in `machines.yml`, no Java required
- `MachineEngine` — async machine processing
- Multiblock crafting stations with YAML recipe format (`infinity_recipes/`)
- GUI-based machine interaction with `machines-gui.yml`

### Energy System

- Energy generators: Solar Panels, Coal Generators
- Cable-based energy transport with configurable loss per block
- Capacitors for energy storage
- ME networks for item storage at scale

---

## [1.x] — Legacy (Slimefun4 Base)

> The 1.x series was a direct fork/extension of Slimefun4. It has been fully superseded by the 2.0 modular rewrite.

- Original custom item definitions ported from Slimefun4
- Basic machine implementations
- Early economy and chat integrations

---

## Upgrade Notes

### Migrating from 1.x to 2.0

!!! warning
    The 2.0 rewrite is **not backward-compatible** with 1.x data files.

1. Back up your entire server
2. Remove the old `NexusSlime` plugin folder
3. Install the 2.0 JAR and start fresh — configs are auto-generated
4. Manually migrate player data if needed using the `NexusItemMigrator` utility
5. Re-apply your custom `items.yml` and recipe definitions

---

## Upcoming / Planned

- Public addon API documentation and example addon
- In-game admin panel GUI
- Dynamic ore generation tweaks via `world-generation` config
- Additional research tiers beyond Infinity
- MySQL cluster support for large multi-server networks

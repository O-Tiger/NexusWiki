# Getting Started

This page covers everything you need to install and configure NexusSlime on your server.

---

## Requirements

| Requirement | Version |
| --- | --- |
| Minecraft Server | Paper / Spigot 1.21+ |
| Java | 17 or newer |
| Soft dependency | PlaceholderAPI (recommended) |
| Soft dependency | LuckPerms (recommended) |
| Soft dependency | SkinsRestorer (optional) |

!!! warning "Cracked Server Notice"
    If your server runs in offline mode (cracked), the **Security module** auth system is mandatory. Premium accounts are detected automatically via the Mojang API and bypass the login screen.

---

## Installation

1. Download the latest `NexusSlime.jar` from the [GitHub Releases](https://github.com/O-Tiger/NexusSlime/releases) page.
2. Place the JAR in your server's `plugins/` folder.
3. Start the server once to generate all default configuration files.
4. Stop the server, edit the generated configs (see below), then restart.

```tree
plugins/
└── NexusSlime/
    ├── config.yml
    ├── items.yml
    ├── machines.yml
    ├── lang/
    │   ├── en_US.yml
    │   ├── pt_BR.yml
    │   └── ...
    ├── security/
    ├── clans/
    ├── economy/
    ├── discord/
    ├── votifier/
    └── ...
```

---

## Main Configuration (`config.yml`)

```yaml
settings:
  language: en_US         # en_US | pt_BR | es_ES | zh_CN
  debug: false
  auto-save-interval: 300 # seconds

database:
  type: SQLITE            # SQLITE or MYSQL

  mysql:                  # Only used when type: MYSQL
    host: localhost
    port: 3306
    database: nexusslime
    username: root
    password: password
    pool-size: 10

resourcepack:
  enabled: false
  url: ""
  sha1: ""
  force: false
  send-on-join: true

energy:
  enabled: true
  max-transfer: 1000
  loss-percentage: 5
  tick-rate: 20

machines:
  enabled: true
  max-per-chunk: 50
  tick-rate: 20
```

---

## Maven Modules

NexusSlime is a **multi-module Maven project**. All modules are bundled into the final plugin JAR automatically.

| Module | Description |
| --- | --- |
| `nexusslime-api` | Public API — interfaces for addon developers |
| `nexusslime-core` | Core managers, PDC registry, language system |
| `nexusslime-items` | Data-driven custom item storage |
| `nexusslime-machines` | Machine definitions and processing engine |
| `nexusslime-systems` | Energy network implementation |
| `nexusslime-integrations` | PlaceholderAPI, LuckPerms, SkinsRestorer hooks |
| `nexusslime-storage` | SQLite / PostgreSQL data persistence |
| `nexusslime-gui` | GUI framework (menus and interfaces) |
| `nexusslime-utils` | Utility helpers |
| `nexusslime-web` | Webstore bridge, VIP kits, payment handling |
| `nexusslime-plugin` | Main entry point, command handler |
| `nexusslime-discord` | JDA Discord bot, webhooks, account linking |
| `nexusslime-chat` | 4-channel chat system with moderation |
| `nexusslime-ae` | ME (Applied Energistics-style) network storage |
| `nexusslime-energy` | Energy generators and cable networks |
| `nexusslime-waila` | WAILA/HUD tooltips |
| `nexusslime-security` | BCrypt auth, anti-bot, anti-lag, anti-dupe |
| `nexusslime-clans` | Clans, territory claiming, upgrades |
| `nexusslime-economy` | Money, credits, /sell, /baltop |
| `nexusslime-essentials` | 40+ QoL commands |
| `nexusslime-crystaldefense` | Wave-based Crystal Defense minigame |
| `nexusslime-custommobs` | YAML-defined custom bosses |
| `nexusslime-dreams` | Sleep cutscene system |
| `nexusslime-protections` | Region protection, flags, duel system |
| `nexusslime-ss` | Silk Spawner support |
| `nexusslime-votifier` | Standalone Votifier V1/V2 server |
| `nexusslime-twitch` | Twitch integration (live alerts, giveaways) |

---

## Building from Source

```bash
git clone https://github.com/O-Tiger/NexusSlime.git
cd NexusSlime
mvn clean package -DskipTests
# Output: nexusslime-plugin/target/NexusSlime-<version>.jar
```

---

## First Steps After Install

1. **Set your language** in `config.yml` → `settings.language`
2. **Configure the Security module** (`security/auth.yml`) if running offline/cracked
3. **Configure the Economy module** (`economy/sell-prices.yml`) with your item prices
4. **Set up Discord** (`discord/config.yml`) with your bot token and channel IDs
5. **Set up Votifier** (`votifier/config.yml`) with your vote links and rewards
6. Give yourself `nexusslime.admin.*` or use LuckPerms to assign permission groups

!!! tip "Reload command"
    After changing any config file, run `/nexusslime reload` to apply changes without restarting.

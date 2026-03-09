# Clans Module

The Clans module lets players create persistent teams with **territory claiming**, **upgrade trees**, a **shared clan chest**, and **clan chat**.

---

## Overview

- Players create or join clans using `/clan`
- Clans can claim chunks as territory
- Territory protects against non-member interaction (configurable)
- Clans level up through the upgrade tree (more members, more chunks)
- A shared clan chest GUI stores items for all members

---

## Commands

| Command | Usage | Permission |
| --- | --- | --- |
| `/clan create <name> <tag>` | Create a new clan | `nexusslime.clan.use` |
| `/clan disband` | Disband your clan | `nexusslime.clan.use` |
| `/clan invite <player>` | Invite a player | `nexusslime.clan.use` |
| `/clan join <name>` | Join a clan by invite | `nexusslime.clan.use` |
| `/clan leave` | Leave your clan | `nexusslime.clan.use` |
| `/clan kick <player>` | Kick a member | `nexusslime.clan.use` |
| `/clan promote <player>` | Promote to officer | `nexusslime.clan.use` |
| `/clan demote <player>` | Demote to member | `nexusslime.clan.use` |
| `/clan info [name]` | View clan info | `nexusslime.clan.use` |
| `/clan list` | List all clans | `nexusslime.clan.use` |
| `/clan chat` | Toggle clan chat | `nexusslime.clan.use` |
| `/clan claim` | Claim current chunk | `nexusslime.clan.use` |
| `/clan unclaim` | Unclaim current chunk | `nexusslime.clan.use` |
| `/clan map` | Show territory map | `nexusslime.clan.use` |
| `/clan chest` | Open clan chest | `nexusslime.clan.use` |
| `/clan upgrade` | Open upgrade menu | `nexusslime.clan.use` |
| `/clan top` | Clan leaderboard | `nexusslime.clan.use` |
| `/clan admin disband <name>` | Force-disband (admin) | `nexusslime.clan.admin` |
| `/clan admin unclaim <name>` | Force-unclaim (admin) | `nexusslime.clan.admin` |

---

## Roles

| Role | Permissions |
| --- | --- |
| **Owner** | All actions, disband, upgrade |
| **Officer** | Invite, kick members, manage territory |
| **Member** | Access chest, chat, use territory |

---

## Territory System

Clans claim chunks as territory. Members can build freely; non-members are blocked (when protection is enabled).

### Territory Configuration (`clans/config.yml`)

```yaml
pvp-friendly-fire: false       # Members cannot damage each other

clan-name-min-length: 3
clan-name-max-length: 16
clan-tag-min-length: 2
clan-tag-max-length: 4

base-member-cap: 10            # Members at level 1
base-territory-cap: 10         # Claimable chunks at level 1

neutral-chunk-protection: false # Protect unclaimed chunks from outsiders

territory-worlds:
  - world
  - world_nether
```

---

## Upgrade Tree (`clans/upgrades.yml`)

Clans spend resources to unlock upgrades that increase their capabilities.

```yaml
upgrades:
  member_cap:
    display-name: "&aMember Expansion"
    description: "Increase maximum members by 5."
    max-level: 5
    cost-per-level:
      money: 5000
    bonus-per-level:
      members: 5

  territory_cap:
    display-name: "&aTerritory Expansion"
    description: "Claim 10 additional chunks per level."
    max-level: 10
    cost-per-level:
      money: 3000
    bonus-per-level:
      chunks: 10

  chest_slots:
    display-name: "&aClan Chest Expansion"
    description: "Add 9 more slots to the clan chest."
    max-level: 5
    cost-per-level:
      money: 2000
    bonus-per-level:
      slots: 9
```

---

## Clan Chest

The clan chest is a shared GUI inventory accessible to all clan members. Its size grows with the `chest_slots` upgrade.

---

## Clan Chat

Toggle clan-only chat with `/clan chat`. Messages sent while in clan chat mode are only visible to clan members.

---

## Permissions

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.clan.use` | Use clan commands | true |
| `nexusslime.clan.admin` | Admin clan management | OP |
| `nexusslime.clan.bypass-protection` | Bypass clan territory protection | OP |

---

## PlaceholderAPI

| Placeholder | Description |
| --- | --- |
| `%nexusslime_clan_name%` | Player's clan name |
| `%nexusslime_clan_tag%` | Clan tag (e.g. `[TAG]`) |
| `%nexusslime_clan_role%` | Player's role in clan |
| `%nexusslime_clan_level%` | Clan level |
| `%nexusslime_clan_members%` | Online member count |
| `%nexusslime_clan_bank%` | Clan bank balance |

See the full [PlaceholderAPI reference](../reference/placeholders.md).

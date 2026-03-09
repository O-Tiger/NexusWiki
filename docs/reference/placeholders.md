# PlaceholderAPI Reference

NexusSlime registers its own PlaceholderAPI expansion under the `nexusslime` identifier. All placeholders follow the pattern `%nexusslime_<name>%`.

**Requires:** [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) (soft dependency — install separately)

---

## Economy

| Placeholder | Description | Example |
| --- | --- | --- |
| `%nexusslime_money%` | Player's current money balance | `12500.00` |
| `%nexusslime_credits%` | Player's credit balance | `350` |

---

## Essentials

| Placeholder | Description | Example |
| --- | --- | --- |
| `%nexusslime_playtime%` | Total playtime (formatted) | `3d 12h 45m` |
| `%nexusslime_playtime_minutes%` | Total playtime in minutes | `5085` |
| `%nexusslime_homes%` | Number of homes set | `3` |
| `%nexusslime_afk%` | `true` if player is AFK | `false` |
| `%nexusslime_afk_status%` | Human-readable AFK status | `AFK` / `Online` |

---

## Clans

| Placeholder | Description | Example |
| --- | --- | --- |
| `%nexusslime_clan_name%` | Player's clan name | `Shadowborn` |
| `%nexusslime_clan_tag%` | Clan tag | `SHD` |
| `%nexusslime_clan_role%` | Player's role in clan | `Owner` / `Officer` / `Member` |
| `%nexusslime_clan_level%` | Clan's current level | `5` |
| `%nexusslime_clan_members%` | Online member count | `8` |
| `%nexusslime_clan_bank%` | Clan bank balance | `75000.00` |

Returns empty string if the player is not in a clan.

---

## Crystal Defense

| Placeholder | Description | Example |
| --- | --- | --- |
| `%nexusslime_crystal_wave%` | Current wave number | `7` |
| `%nexusslime_crystal_health%` | Crystal HP remaining | `680.0` |
| `%nexusslime_crystal_points%` | Player's kill points in current game | `145` |
| `%nexusslime_crystal_arena%` | Arena name the player is in | `arena1` |

Returns empty string if the player is not in a Crystal Defense game.

---

## Security

| Placeholder | Description | Example |
| --- | --- | --- |
| `%nexusslime_authenticated%` | `true` if the player is logged in | `true` |
| `%nexusslime_auth_status%` | Human-readable auth status | `Authenticated` / `Pending` |

---

## Votifier

| Placeholder | Description | Example |
| --- | --- | --- |
| `%nexusslime_votes_total%` | Total lifetime votes | `127` |
| `%nexusslime_vote_streak%` | Current vote streak length | `12` |

---

## Player Stats

| Placeholder | Description | Example |
| --- | --- | --- |
| `%nexusslime_player_blocks_broken%` | Total blocks broken | `48320` |
| `%nexusslime_player_machines_placed%` | Total machines placed | `214` |
| `%nexusslime_player_items_crafted%` | Total items crafted | `5630` |
| `%nexusslime_player_energy_generated%` | Total energy generated (RF) | `1200000` |
| `%nexusslime_player_items_smelted%` | Total items smelted | `890` |
| `%nexusslime_player_research_unlocked%` | Research entries unlocked | `34` |
| `%nexusslime_player_level%` | Player NexusSlime level | `15` |
| `%nexusslime_researched_<id>%` | `true` if a specific research is unlocked | `true` |

---

## Backpacks

| Placeholder | Description | Example |
| --- | --- | --- |
| `%nexusslime_backpacks_owned%` | Number of backpacks the player owns | `2` |

---

## Machines

| Placeholder | Description | Example |
| --- | --- | --- |
| `%nexusslime_machines_count%` | Total machines placed by player | `42` |

---

## LuckPerms

| Placeholder | Description | Example |
| --- | --- | --- |
| `%nexusslime_lp_prefix%` | Player's LuckPerms prefix | `&6[VIP]` |
| `%nexusslime_lp_suffix%` | Player's LuckPerms suffix | `&7✦` |

These require LuckPerms to be installed.

---

## Guide

| Placeholder | Description |
| --- | --- |
| `%nexusslime_guide_<id>%` | Dynamic guide entry for item/machine ID |

These are dynamic — replace `<id>` with any registered item or machine ID.

---

## Core / Misc

| Placeholder | Description | Example |
| --- | --- | --- |
| `%nexusslime_version%` | Plugin version string | `2.0.0-BETA` |
| `%nexusslime_player%` | Player username | `Steve` |
| `%nexusslime_uuid%` | Player UUID | `069a79f4-...` |

---

## Usage in Scoreboards / TAB

```yaml
# Example with TAB plugin
header: "&bNexusSlime &7%nexusslime_version%"
tablist-name: "%nexusslime_lp_prefix%%player_name%"
scoreboard:
  title: "&b&lYour Stats"
  lines:
    - "&7Money: &a$%nexusslime_money%"
    - "&7Credits: &b%nexusslime_credits%"
    - "&7Votes: &e%nexusslime_votes_total% &7(streak: %nexusslime_vote_streak%)"
    - "&7Clan: &f%nexusslime_clan_name%"
    - "&7Playtime: &f%nexusslime_playtime%"
```

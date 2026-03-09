# Economy Module

The Economy module provides a **dual-currency system** (money and credits), sell commands, a wealth leaderboard, and per-item sell price configuration.

---

## Overview

| Currency | Description |
| --- | --- |
| **Money** (`$`) | Standard in-game currency earned from selling items, voting, etc. |
| **Credits** | Premium currency typically obtained from the webstore |

---

## Commands

| Command | Usage | Permission |
| --- | --- | --- |
| `/money` | Check your balance | `nexusslime.economy.money` |
| `/money <player>` | Check another player's balance | `nexusslime.economy.money` |
| `/credits` | Check your credits | `nexusslime.economy.credits` |
| `/credits <player>` | Check another's credits | `nexusslime.economy.credits` |
| `/baltop` | Top 10 richest players | `nexusslime.economy.baltop` |
| `/sell hand` | Sell item in hand | `nexusslime.economy.sell` |
| `/sell all` | Sell all sellable items | `nexusslime.economy.sell` |
| `/sell inventory` | Sell entire inventory | `nexusslime.economy.sell` |
| `/worth [item]` | Check sell value of item | `nexusslime.essentials.worth` |
| `/eco give <player> <amount>` | Give money (admin) | `nexusslime.economy.admin` |
| `/eco take <player> <amount>` | Take money (admin) | `nexusslime.economy.admin` |
| `/eco set <player> <amount>` | Set balance (admin) | `nexusslime.economy.admin` |
| `/eco reset <player>` | Reset balance (admin) | `nexusslime.economy.admin` |

---

## Permissions

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.economy.money` | Check balances | true |
| `nexusslime.economy.credits` | Check credits | true |
| `nexusslime.economy.baltop` | View leaderboard | true |
| `nexusslime.economy.sell` | Use /sell commands | true |
| `nexusslime.economy.admin` | Admin eco commands | OP |

---

## Sell Prices (`economy/sell-prices.yml`)

Configure per-material sell prices used by `/sell` and `/worth`.

```yaml
prices:
  # ── Stone & Earth ──────────────────────────────────────────────
  COBBLESTONE:       2.0
  STONE:             3.0
  DIRT:              1.0
  GRAVEL:            1.5
  SAND:              2.0

  # ── Wood & Plants ──────────────────────────────────────────────
  OAK_LOG:           6.0
  SPRUCE_LOG:        6.0
  WHEAT:             4.0
  SUGAR_CANE:        3.0

  # ── Ores & Metals ──────────────────────────────────────────────
  COAL:             10.0
  RAW_IRON:         15.0
  IRON_INGOT:       25.0
  RAW_GOLD:         30.0
  GOLD_INGOT:       50.0
  DIAMOND:         200.0
  EMERALD:         100.0
  NETHERITE_INGOT: 1200.0

  # ── Mob Drops ──────────────────────────────────────────────────
  BONE:              5.0
  ROTTEN_FLESH:      2.0
  BLAZE_ROD:        20.0
  ENDER_PEARL:      25.0
  SHULKER_SHELL:   150.0
  HEART_OF_THE_SEA: 500.0

  # Set to 0 or omit to make an item unsellable
  BEDROCK:           0.0
```

!!! tip
    Use Material names (Bukkit uppercase). Items not listed in `sell-prices.yml` cannot be sold. Custom NexusSlime items can also be added by their item ID.

---

## PlaceholderAPI

| Placeholder | Description |
| --- | --- |
| `%nexusslime_money%` | Player's money balance |
| `%nexusslime_credits%` | Player's credit balance |

See the full [PlaceholderAPI reference](../reference/placeholders.md).

# Essentials Module

The Essentials module provides **40+ quality-of-life commands** covering homes, warps, waypoints, teleportation, AFK detection, jail, and everyday utility commands.

---

## Homes

Players can set named homes and teleport back to them.

### Commands

| Command | Usage | Permission |
| --- | --- | --- |
| `/home [name]` | Teleport to a home | `nexusslime.essentials.home` |
| `/home list` | List all homes | `nexusslime.essentials.home` |
| `/sethome <name>` | Set a home at your location | `nexusslime.essentials.home` |
| `/delhome <name>` | Delete a home | `nexusslime.essentials.home` |

### Home Slot Permissions

| Permission | Slots |
| --- | --- |
| `nexusslime.essentials.homes.1` | 1 (default: true) |
| `nexusslime.essentials.homes.3` | 3 |
| `nexusslime.essentials.homes.10` | 10 |
| `nexusslime.essentials.homes.unlimited` | Unlimited (OP) |

---

## Warps

Server-wide public teleport destinations managed by admins.

## Warps Commands

| Command | Usage | Permission |
| --- | --- | --- |
| `/warp <name>` | Teleport to a warp | `nexusslime.essentials.warp.use` |
| `/warp list` | List all warps | `nexusslime.essentials.warp.use` |
| `/setwarp <name>` | Create a warp | `nexusslime.essentials.warp.admin` |
| `/delwarp <name>` | Delete a warp | `nexusslime.essentials.warp.admin` |

---

## TPA (Teleport Requests)

### TPA Commands

| Command | Usage | Permission |
| --- | --- | --- |
| `/tpa <player>` | Send a teleport request | `nexusslime.essentials.tpa` |
| `/tpaccept` | Accept a teleport request | `nexusslime.essentials.tpa` |
| `/tpdeny` | Deny a teleport request | `nexusslime.essentials.tpa` |
| `/tphere <player>` | Teleport a player to you | `nexusslime.essentials.tphere` |
| `/tppos <x> <y> <z>` | Teleport to coordinates | `nexusslime.essentials.tppos` |
| `/spawn` | Teleport to spawn | `nexusslime.essentials.spawn` |
| `/setspawn` | Set the server spawn | `nexusslime.essentials.setspawn` |
| `/back` | Return to previous location | `nexusslime.essentials.back` |

### TPA Configuration (`essentials/config.yml`)

```yaml
tpa:
  expiry-seconds: 60       # Request expires after this many seconds

back:
  save-on-death: true      # Save death location for /back
  save-on-any-teleport: false

spawn:
  respawn-at-spawn: false  # Force respawn at spawn (vs. bed)
```

---

## AFK System

### AFK Commands

| Command | Usage | Permission |
| --- | --- | --- |
| `/afk` | Toggle AFK status | `nexusslime.essentials.afk` |

### AFK Configuration

```yaml
afk:
  idle-seconds: 300        # Auto-AFK after 5 minutes of inactivity
  broadcast: true          # Announce when a player goes AFK
```

---

## Jail

Admins can send players to a predefined jail location.

### Jail Commands

| Command | Usage | Permission |
| --- | --- | --- |
| `/jail <player> [duration]` | Jail a player | `nexusslime.essentials.jail.admin` |
| `/unjail <player>` | Release a player | `nexusslime.essentials.jail.admin` |
| `/setjail` | Set the jail location | `nexusslime.essentials.jail.admin` |

---

## Utility Commands

| Command | Usage | Permission |
| --- | --- | --- |
| `/fly` | Toggle fly mode | `nexusslime.essentials.fly` |
| `/fly <player>` | Toggle fly for another player | `nexusslime.essentials.fly.others` |
| `/god` | Toggle god mode | `nexusslime.essentials.god` |
| `/god <player>` | Toggle god for another player | `nexusslime.essentials.god.others` |
| `/heal` | Heal yourself | `nexusslime.essentials.heal` |
| `/heal <player>` | Heal another player | `nexusslime.essentials.heal.others` |
| `/feed` | Feed yourself | `nexusslime.essentials.feed` |
| `/feed <player>` | Feed another player | `nexusslime.essentials.feed.others` |
| `/nick <name>` | Set your nickname | `nexusslime.essentials.nick` |
| `/nick <player> <name>` | Set another player's nick | `nexusslime.essentials.nick.others` |
| `/workbench` | Open a portable workbench | `nexusslime.essentials.workbench` |
| `/trash` | Open a portable trash bin | `nexusslime.essentials.trash` |
| `/anvil` | Open a portable anvil | `nexusslime.essentials.anvil` |
| `/grindstone` | Open a portable grindstone | `nexusslime.essentials.grindstone` |
| `/stonecutter` | Open a portable stonecutter | `nexusslime.essentials.stonecutter` |
| `/speed <value>` | Set walk/fly speed | `nexusslime.essentials.speed` |
| `/near` | List nearby players | `nexusslime.essentials.near` |
| `/seen <player>` | Last seen info | `nexusslime.essentials.seen` |
| `/clearinventory` | Clear your inventory | `nexusslime.essentials.clearinventory` |
| `/clearinventory <player>` | Clear another's inventory | `nexusslime.essentials.clearinventory.others` |
| `/getpos` | Show your coordinates | `nexusslime.essentials.getpos` |
| `/playtime` | Check your playtime | `nexusslime.essentials.playtime` |
| `/gamemode <mode>` | Change gamemode | `nexusslime.essentials.gamemode` |
| `/enderchest` | Open your ender chest | `nexusslime.essentials.enderchest` |
| `/enderchest <player>` | Open another's ender chest | `nexusslime.essentials.enderchest.others` |
| `/repair` | Repair held item | `nexusslime.essentials.repair` |
| `/ext` | Extinguish yourself | `nexusslime.essentials.ext` |
| `/exp <amount>` | Give yourself XP | `nexusslime.essentials.exp` |
| `/hat` | Wear held item as hat | `nexusslime.essentials.hat` |
| `/skull <player>` | Get a player's head | `nexusslime.essentials.skull` |
| `/rules` | Show server rules | `nexusslime.essentials.rules` |
| `/worth [item]` | Check item sell value | `nexusslime.essentials.worth` |

### Server Rules Configuration

```yaml
rules:
  - "&7 1. Respect all players."
  - "&7 2. No griefing or stealing."
  - "&7 3. No hacking or exploiting."
  - "&7 4. Have fun!"
```

### Fly Configuration

```yaml
fly:
  deny-in-pvp-regions: true   # Disable /fly when entering PvP regions
```

# Permissions Reference

Complete list of all permission nodes registered by NexusSlime. Nodes marked **OP** default to operators only; nodes marked **true** are granted to all players by default.

---

## Core & Admin

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.*` | All permissions | OP |
| `nexusslime.command` | Use basic `/nexusslime` command | true |
| `nexusslime.admin` | General admin access | OP |
| `nexusslime.admin.*` | All admin permissions | OP |
| `nexusslime.admin.reload` | Reload plugin configs | OP |
| `nexusslime.admin.give` | Give custom items | OP |
| `nexusslime.admin.debug` | Toggle debug mode | OP |
| `nexusslime.admin.cleardata` | Clear player data | OP |
| `nexusslime.bypass.protection` | Bypass all region protections | OP |

---

## Research

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.research` | Access research system | true |
| `nexusslime.research.all` | Instantly unlock all research | OP |

---

## Backpacks

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.backpack.create` | Create backpacks | true |
| `nexusslime.backpack.upgrade` | Upgrade backpacks | true |
| `nexusslime.backpack.unlimited` | Unlimited backpack slots | OP |

---

## Waypoints

| Permission | Slots | Default |
| --- | --- | --- |
| `nexusslime.essentials.waypoints.1` | 1 waypoint | true |
| `nexusslime.essentials.waypoints.5` | 5 waypoints | — |
| `nexusslime.essentials.waypoints.25` | 25 waypoints | — |
| `nexusslime.essentials.waypoints.unlimited` | Unlimited | OP |
| `nexusslime.essentials.waypoint` | Access waypoint commands | true |

---

## Homes

| Permission | Slots | Default |
| --- | --- | --- |
| `nexusslime.essentials.homes.1` | 1 home | true |
| `nexusslime.essentials.homes.3` | 3 homes | — |
| `nexusslime.essentials.homes.10` | 10 homes | — |
| `nexusslime.essentials.homes.unlimited` | Unlimited | OP |
| `nexusslime.essentials.home` | Use /home, /sethome, /delhome | true |

---

## Essentials Commands

| Permission | Command | Default |
| --- | --- | --- |
| `nexusslime.essentials.warp.use` | `/warp` | true |
| `nexusslime.essentials.warp.admin` | `/setwarp`, `/delwarp` | OP |
| `nexusslime.essentials.back` | `/back` | true |
| `nexusslime.essentials.tpa` | `/tpa`, `/tpaccept`, `/tpdeny` | true |
| `nexusslime.essentials.spawn` | `/spawn` | true |
| `nexusslime.essentials.setspawn` | `/setspawn` | OP |
| `nexusslime.essentials.tphere` | `/tphere` | OP |
| `nexusslime.essentials.tppos` | `/tppos` | OP |
| `nexusslime.essentials.near` | `/near` | true |
| `nexusslime.essentials.fly` | `/fly` (self) | false |
| `nexusslime.essentials.fly.others` | `/fly <player>` | OP |
| `nexusslime.essentials.hat` | `/hat` | false |
| `nexusslime.essentials.god` | `/god` (self) | OP |
| `nexusslime.essentials.god.others` | `/god <player>` | OP |
| `nexusslime.essentials.heal` | `/heal` (self) | OP |
| `nexusslime.essentials.heal.others` | `/heal <player>` | OP |
| `nexusslime.essentials.feed` | `/feed` (self) | OP |
| `nexusslime.essentials.feed.others` | `/feed <player>` | OP |
| `nexusslime.essentials.nick` | `/nick` (self) | false |
| `nexusslime.essentials.nick.others` | `/nick <player>` | OP |
| `nexusslime.essentials.afk` | `/afk` | true |
| `nexusslime.essentials.workbench` | `/workbench` | true |
| `nexusslime.essentials.trash` | `/trash` | true |
| `nexusslime.essentials.anvil` | `/anvil` | OP |
| `nexusslime.essentials.grindstone` | `/grindstone` | OP |
| `nexusslime.essentials.stonecutter` | `/stonecutter` | OP |
| `nexusslime.essentials.speed` | `/speed` | OP |
| `nexusslime.essentials.seen` | `/seen` | true |
| `nexusslime.essentials.clearinventory` | `/clearinventory` (self) | OP |
| `nexusslime.essentials.clearinventory.others` | `/clearinventory <player>` | OP |
| `nexusslime.essentials.getpos` | `/getpos` | true |
| `nexusslime.essentials.playtime` | `/playtime` | true |
| `nexusslime.essentials.gamemode` | `/gamemode` | OP |
| `nexusslime.essentials.enderchest` | `/enderchest` (self) | true |
| `nexusslime.essentials.enderchest.others` | `/enderchest <player>` | OP |
| `nexusslime.essentials.repair` | `/repair` | OP |
| `nexusslime.essentials.ext` | `/ext` | OP |
| `nexusslime.essentials.exp` | `/exp` | OP |
| `nexusslime.essentials.worth` | `/worth` | true |
| `nexusslime.essentials.rules` | `/rules` | true |
| `nexusslime.essentials.skull` | `/skull` | OP |
| `nexusslime.essentials.jail.admin` | Jail management | OP |
| `nexusslime.essentials.backpack` | Backpack commands | true |

---

## Economy

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.economy.money` | View money balance | true |
| `nexusslime.economy.credits` | View credits | true |
| `nexusslime.economy.baltop` | View leaderboard | true |
| `nexusslime.economy.sell` | Use /sell | true |
| `nexusslime.economy.admin` | Admin eco commands | OP |

---

## Clans

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.clan.use` | Use clan commands | true |
| `nexusslime.clan.admin` | Admin clan management | OP |
| `nexusslime.clan.bypass-protection` | Bypass clan territory | OP |

---

## Security

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.security.cleanworld` | Manual world cleaner | OP |
| `nexusslime.staff.vanish` | Vanish yourself | OP |
| `nexusslime.staff.vanish.others` | Vanish another player | OP |
| `nexusslime.staff.vanish.see` | See vanished players | OP |
| `nexusslime.staff.invsee` | Inspect inventories | OP |
| `nexusslime.staff.spy` | Chat spy mode | OP |

---

## Chat

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.chat.staff` | Access staff chat channel | OP |
| `nexusslime.chat.mute` | Mute players | OP |
| `nexusslime.chat.mute.bypass` | Bypass mute | false |
| `nexusslime.chat.filter.bypass` | Bypass word filter | OP |
| `nexusslime.chat.reload` | Reload chat config | OP |
| `nexusslime.chat.color` | Use color codes in chat | OP |

---

## Protections & Duel

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.region.use` | Create and manage own regions | true |
| `nexusslime.protect.admin` | Admin region management | OP |
| `nexusslime.duel.use` | Send and accept duels | true |

---

## Crystal Defense

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.crystaldefense.use` | Join arenas | true |
| `nexusslime.crystaldefense.admin` | Create/manage arenas | OP |

---

## Votifier

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.vote` | Use `/vote` | true |
| `nexusslime.vote.top` | Use `/votetop` | true |

---

## Custom Mobs

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.boss.admin` | All boss/spawn-egg commands | OP |

---

## Dreams

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.dreams.admin` | Admin dreams commands | OP |

---

## Twitch

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.twitch.use` | Basic Twitch commands | true |
| `nexusslime.twitch.staff` | Approve links, run giveaways | OP |
| `nexusslime.twitch.admin` | Reload Twitch config | OP |

---

## Silk Spawners

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.silkspawner.use` | Mine spawners with Silk Touch | true |
| `nexusslime.silkspawner.admin` | Admin spawner commands | OP |

---

## Recipes & Kits

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.recipe` | Use `/recipe` | true |
| `nexusslime.command.kit` | Use `/kit` | true |
| `nexusslime.command.vip` | Use `/vip` | true |
| `nexusslime.kit.*` | Access all VIP kits | OP |

---

## Permission Level Nodes

Used internally to map staff ranks. Configure in `config.yml`:

| Permission | Rank |
| --- | --- |
| `nexusslime.level.user` | Regular player |
| `nexusslime.level.helper` | Helper |
| `nexusslime.level.moderator` | Moderator |
| `nexusslime.level.admin` | Admin |
| `nexusslime.level.owner` | Owner |

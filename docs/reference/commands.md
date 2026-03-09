# Commands Reference

Complete list of all commands registered by NexusSlime, organized by module.

**Legend:**

- `<arg>` — required argument
- `[arg]` — optional argument
- `(OP)` — operator-only by default
- `(true)` — available to all players by default

---

## Core / Plugin

| Command | Aliases | Description | Permission |
| --- | --- | --- | --- |
| `/nexusslime help` | `/ns`, `/nexus`, `/slime` | Show help | `nexusslime.command` |
| `/nexusslime info` | | Plugin version and status | `nexusslime.command` |
| `/nexusslime reload` | | Reload all configs | `nexusslime.admin.reload` |
| `/nexusslime give <player> <item>` | | Give a custom item | `nexusslime.admin.give` |
| `/nexusslime guide` | | Open item guide GUI | `nexusslime.command` |
| `/nexusslime modules` | | List all loaded modules | `nexusslime.command` |
| `/nexusslime machine info <id>` | | Machine details | `nexusslime.command` |
| `/nexusslime machine list` | | List all machines | `nexusslime.command` |
| `/nexusslime energy info <x,y,z>` | | Energy node info | `nexusslime.command` |
| `/nexusslime energy network` | | View energy network | `nexusslime.command` |
| `/research` | | View your research progress | `nexusslime.research` |
| `/research list [tier]` | | List research by tier | `nexusslime.research` |
| `/research <item-id>` | | Check specific research | `nexusslime.research` |
| `/recipe <item>` | | Show crafting recipe(s) | `nexusslime.recipe` |

---

## Backpacks & Waypoints

| Command | Aliases | Description | Permission |
| --- | --- | --- | --- |
| `/backpack open [id]` | | Open your backpack | `nexusslime.essentials.backpack` |
| `/backpack list` | | List all backpacks | `nexusslime.essentials.backpack` |
| `/waypoint create <name>` | `/wp` | Create a waypoint | `nexusslime.essentials.waypoint` |
| `/waypoint delete <name>` | `/wp` | Delete a waypoint | `nexusslime.essentials.waypoint` |
| `/waypoint list` | `/wp` | List all waypoints | `nexusslime.essentials.waypoint` |
| `/waypoint tp <name>` | `/wp` | Teleport to waypoint | `nexusslime.essentials.waypoint` |
| `/waypoint info <name>` | `/wp` | Waypoint info | `nexusslime.essentials.waypoint` |

---

## Essentials — Homes

| Command | Description | Permission |
| --- | --- | --- |
| `/home [name]` | Teleport to a home | `nexusslime.essentials.home` |
| `/home list` | List all homes | `nexusslime.essentials.home` |
| `/sethome <name>` | Set home at current location | `nexusslime.essentials.home` |
| `/delhome <name>` | Delete a home | `nexusslime.essentials.home` |

---

## Essentials — Warps

| Command | Description | Permission |
| --- | --- | --- |
| `/warp <name>` | Teleport to a warp | `nexusslime.essentials.warp.use` |
| `/warp list` | List all warps | `nexusslime.essentials.warp.use` |
| `/setwarp <name>` | Create a warp (OP) | `nexusslime.essentials.warp.admin` |
| `/delwarp <name>` | Delete a warp (OP) | `nexusslime.essentials.warp.admin` |

---

## Essentials — Teleportation

| Command | Description | Permission |
| --- | --- | --- |
| `/tpa <player>` | Send teleport request | `nexusslime.essentials.tpa` |
| `/tpaccept` | Accept teleport request | `nexusslime.essentials.tpa` |
| `/tpdeny` | Deny teleport request | `nexusslime.essentials.tpa` |
| `/tphere <player>` | Summon a player (OP) | `nexusslime.essentials.tphere` |
| `/tppos <x> <y> <z>` | Teleport to coordinates (OP) | `nexusslime.essentials.tppos` |
| `/spawn` | Teleport to spawn | `nexusslime.essentials.spawn` |
| `/setspawn` | Set server spawn (OP) | `nexusslime.essentials.setspawn` |
| `/back` | Return to previous location | `nexusslime.essentials.back` |

---

## Essentials — Utility

| Command | Description | Permission |
| --- | --- | --- |
| `/afk` | Toggle AFK | `nexusslime.essentials.afk` |
| `/fly` | Toggle fly (self) | `nexusslime.essentials.fly` |
| `/fly <player>` | Toggle fly (other, OP) | `nexusslime.essentials.fly.others` |
| `/god` | Toggle god mode | `nexusslime.essentials.god` |
| `/god <player>` | Toggle god (other, OP) | `nexusslime.essentials.god.others` |
| `/heal` | Heal yourself (OP) | `nexusslime.essentials.heal` |
| `/heal <player>` | Heal another (OP) | `nexusslime.essentials.heal.others` |
| `/feed` | Feed yourself (OP) | `nexusslime.essentials.feed` |
| `/feed <player>` | Feed another (OP) | `nexusslime.essentials.feed.others` |
| `/nick <name>` | Set nickname | `nexusslime.essentials.nick` |
| `/nick <player> <name>` | Set nickname (other, OP) | `nexusslime.essentials.nick.others` |
| `/hat` | Wear item as hat | `nexusslime.essentials.hat` |
| `/speed <value>` | Set walk/fly speed (OP) | `nexusslime.essentials.speed` |
| `/workbench` | Portable workbench | `nexusslime.essentials.workbench` |
| `/anvil` | Portable anvil (OP) | `nexusslime.essentials.anvil` |
| `/grindstone` | Portable grindstone (OP) | `nexusslime.essentials.grindstone` |
| `/stonecutter` | Portable stonecutter (OP) | `nexusslime.essentials.stonecutter` |
| `/trash` | Portable trash bin | `nexusslime.essentials.trash` |
| `/near` | List nearby players | `nexusslime.essentials.near` |
| `/seen <player>` | Last seen info | `nexusslime.essentials.seen` |
| `/getpos` | Show coordinates | `nexusslime.essentials.getpos` |
| `/playtime` | Check playtime | `nexusslime.essentials.playtime` |
| `/gamemode <mode>` | Change gamemode (OP) | `nexusslime.essentials.gamemode` |
| `/enderchest` | Open ender chest | `nexusslime.essentials.enderchest` |
| `/enderchest <player>` | Open other's ender chest (OP) | `nexusslime.essentials.enderchest.others` |
| `/clearinventory` | Clear own inventory (OP) | `nexusslime.essentials.clearinventory` |
| `/clearinventory <player>` | Clear other's inventory (OP) | `nexusslime.essentials.clearinventory.others` |
| `/repair` | Repair held item (OP) | `nexusslime.essentials.repair` |
| `/ext` | Extinguish yourself (OP) | `nexusslime.essentials.ext` |
| `/exp <amount>` | Give XP (OP) | `nexusslime.essentials.exp` |
| `/skull [player]` | Get player head (OP) | `nexusslime.essentials.skull` |
| `/rules` | Show server rules | `nexusslime.essentials.rules` |
| `/worth [item]` | Item sell value | `nexusslime.essentials.worth` |

---

## Essentials — Jail

| Command | Description | Permission |
| --- | --- | --- |
| `/jail <player> [duration]` | Jail a player (OP) | `nexusslime.essentials.jail.admin` |
| `/unjail <player>` | Release a player (OP) | `nexusslime.essentials.jail.admin` |
| `/setjail` | Set jail location (OP) | `nexusslime.essentials.jail.admin` |

---

## Economy

| Command | Description | Permission |
| --- | --- | --- |
| `/money [player]` | Check balance | `nexusslime.economy.money` |
| `/credits [player]` | Check credits | `nexusslime.economy.credits` |
| `/baltop` | Top 10 richest | `nexusslime.economy.baltop` |
| `/sell hand` | Sell item in hand | `nexusslime.economy.sell` |
| `/sell all` | Sell all sellable items | `nexusslime.economy.sell` |
| `/sell inventory` | Sell entire inventory | `nexusslime.economy.sell` |
| `/worth [item]` | Check sell value | `nexusslime.essentials.worth` |
| `/eco give <player> <amount>` | Give money (OP) | `nexusslime.economy.admin` |
| `/eco take <player> <amount>` | Take money (OP) | `nexusslime.economy.admin` |
| `/eco set <player> <amount>` | Set balance (OP) | `nexusslime.economy.admin` |
| `/eco reset <player>` | Reset balance (OP) | `nexusslime.economy.admin` |

---

## Clans

| Command | Description | Permission |
| --- | --- | --- |
| `/clan create <name> <tag>` | Create a clan | `nexusslime.clan.use` |
| `/clan disband` | Disband clan | `nexusslime.clan.use` |
| `/clan invite <player>` | Invite a player | `nexusslime.clan.use` |
| `/clan join <name>` | Join a clan | `nexusslime.clan.use` |
| `/clan leave` | Leave clan | `nexusslime.clan.use` |
| `/clan kick <player>` | Kick a member | `nexusslime.clan.use` |
| `/clan promote <player>` | Promote to officer | `nexusslime.clan.use` |
| `/clan demote <player>` | Demote to member | `nexusslime.clan.use` |
| `/clan info [name]` | Clan info | `nexusslime.clan.use` |
| `/clan list` | List all clans | `nexusslime.clan.use` |
| `/clan chat` | Toggle clan chat | `nexusslime.clan.use` |
| `/clan claim` | Claim current chunk | `nexusslime.clan.use` |
| `/clan unclaim` | Unclaim current chunk | `nexusslime.clan.use` |
| `/clan map` | Show territory map | `nexusslime.clan.use` |
| `/clan chest` | Open clan chest | `nexusslime.clan.use` |
| `/clan upgrade` | Open upgrade menu | `nexusslime.clan.use` |
| `/clan top` | Clan leaderboard | `nexusslime.clan.use` |
| `/clan admin disband <name>` | Force disband (OP) | `nexusslime.clan.admin` |
| `/clan admin unclaim <name>` | Force unclaim (OP) | `nexusslime.clan.admin` |

---

## Security & Staff

| Command | Description | Permission |
| --- | --- | --- |
| `/register <password> <confirm>` | Register account | *(all)* |
| `/login <password>` | Login | *(all)* |
| `/changepassword <old> <new>` | Change password | *(authenticated)* |
| `/vanish` | Toggle vanish (OP) | `nexusslime.staff.vanish` |
| `/vanish <player>` | Vanish other (OP) | `nexusslime.staff.vanish.others` |
| `/invsee <player>` | Inspect inventory (OP) | `nexusslime.staff.invsee` |
| `/spy` | Toggle chat spy (OP) | `nexusslime.staff.spy` |
| `/cleanworld` | Run world cleaner (OP) | `nexusslime.security.cleanworld` |

---

## Discord

| Command | Description | Permission |
| --- | --- | --- |
| `/discord` | Discord invite link | *(all)* |
| `/discord link` | Start account linking | *(all)* |
| `/discord unlink` | Unlink account | *(all)* |
| `/discord info` | Show linked account | *(all)* |
| `/discordrr` | Manage reaction roles (OP) | `nexusslime.admin` |

---

## Protections & Duel

| Command | Description | Permission |
| --- | --- | --- |
| `/region claim <name>` | Claim selected area | `nexusslime.region.use` |
| `/region delete <name>` | Delete region | `nexusslime.region.use` |
| `/region list` | List your regions | `nexusslime.region.use` |
| `/region info [name]` | Region details | `nexusslime.region.use` |
| `/region addmember <region> <player>` | Add member | `nexusslime.region.use` |
| `/region removemember <region> <player>` | Remove member | `nexusslime.region.use` |
| `/region setflag <region> <flag> <val>` | Set a flag | `nexusslime.region.use` |
| `/region flags <region>` | View flags | `nexusslime.region.use` |
| `/protect <name>` | Quick chunk protection | `nexusslime.region.use` |
| `/region admin list` | Admin: all regions (OP) | `nexusslime.protect.admin` |
| `/region admin delete <name>` | Admin: delete region (OP) | `nexusslime.protect.admin` |
| `/duel <player>` | Challenge to duel | `nexusslime.duel.use` |
| `/duel accept` | Accept duel | `nexusslime.duel.use` |
| `/duel deny` | Deny duel | `nexusslime.duel.use` |
| `/duel spectate <player>` | Spectate duel | `nexusslime.duel.use` |
| `/duel stats` | Duel stats | `nexusslime.duel.use` |
| `/duel setarena` | Set duel arena (OP) | `nexusslime.protect.admin` |

---

## Crystal Defense

| Command | Description | Permission |
| --- | --- | --- |
| `/crystal join <arena>` | Join an arena | `nexusslime.crystaldefense.use` |
| `/crystal leave` | Leave arena | `nexusslime.crystaldefense.use` |
| `/crystal list` | List arenas | `nexusslime.crystaldefense.use` |
| `/crystal status` | Wave and crystal HP | `nexusslime.crystaldefense.use` |
| `/crystal create <name>` | Create arena (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal delete <name>` | Delete arena (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal setcrystal <arena>` | Set crystal loc (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal setspawn <arena>` | Set spawn (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal start [arena]` | Force-start (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal stop [arena]` | Stop game (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal reload` | Reload configs (OP) | `nexusslime.crystaldefense.admin` |

---

## Votifier

| Command | Description | Permission |
| --- | --- | --- |
| `/vote` | Show vote links and streak | `nexusslime.vote` |
| `/votetop` | Vote leaderboard | `nexusslime.vote.top` |

---

## Custom Mobs

| Command | Description | Permission |
| --- | --- | --- |
| `/boss spawn <id>` | Spawn a boss | `nexusslime.boss.admin` |
| `/boss spawn <id> <w> <x> <y> <z>` | Spawn at coords | `nexusslime.boss.admin` |
| `/boss list` | List all bosses | `nexusslime.boss.admin` |
| `/boss info <id>` | Boss definition | `nexusslime.boss.admin` |
| `/boss kill <id>` | Kill all boss instances | `nexusslime.boss.admin` |
| `/bossegg give <player> <id>` | Give spawn egg | `nexusslime.boss.admin` |

---

## Dreams

| Command | Description | Permission |
| --- | --- | --- |
| `/dreams reload` | Reload config | `nexusslime.dreams.admin` |
| `/dreams trigger <player>` | Force dream | `nexusslime.dreams.admin` |
| `/dreams trigger <player> nightmare` | Force nightmare | `nexusslime.dreams.admin` |

---

## Twitch

| Command | Description | Permission |
| --- | --- | --- |
| `/twitch link <username>` | Start linking | `nexusslime.twitch.use` |
| `/twitch unlink` | Unlink account | `nexusslime.twitch.use` |
| `/twitch status` | Link status | `nexusslime.twitch.use` |
| `/twitch approve <player>` | Approve link (OP) | `nexusslime.twitch.staff` |
| `/twitch reject <player>` | Reject link (OP) | `nexusslime.twitch.staff` |
| `/twitch pending` | Pending requests (OP) | `nexusslime.twitch.staff` |
| `/twitch giveaway <streamer>` | Draw winner (OP) | `nexusslime.twitch.staff` |
| `/twitch reload` | Reload config (OP) | `nexusslime.twitch.admin` |

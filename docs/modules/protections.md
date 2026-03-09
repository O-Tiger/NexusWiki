# Protections Module

The Protections module provides **player-owned region claiming**, configurable protection flags, and a **1v1 duel system**.

---

## Region Claiming

Players select two corners of a cuboid region with the selection wand, then claim it as their protected area. Non-members cannot build, break, or interact within the region by default.

### How to Claim a Region

1. Hold a **Golden Axe** (default wand)
2. Left-click one corner of your region → right-click the opposite corner
3. Run `/region claim <name>` to claim the selection

### Commands

| Command | Usage | Permission |
| --- | --- | --- |
| `/region claim <name>` | Claim selected area | `nexusslime.region.use` |
| `/region delete <name>` | Delete a region | `nexusslime.region.use` |
| `/region list` | List your regions | `nexusslime.region.use` |
| `/region info [name]` | View region details | `nexusslime.region.use` |
| `/region addmember <region> <player>` | Add a member | `nexusslime.region.use` |
| `/region removemember <region> <player>` | Remove a member | `nexusslime.region.use` |
| `/region setflag <region> <flag> <value>` | Set a flag | `nexusslime.region.use` |
| `/region flags <region>` | View all flags | `nexusslime.region.use` |
| `/protect <name>` | Quick-protect current chunk | `nexusslime.region.use` |
| `/region admin list [player]` | Admin: list all regions | `nexusslime.protect.admin` |
| `/region admin delete <name>` | Admin: force-delete region | `nexusslime.protect.admin` |
| `/region admin setowner <region> <player>` | Admin: change owner | `nexusslime.protect.admin` |

---

## Region Flags

Flags control what is and isn't allowed within a region.

| Flag | Values | Default | Description |
| --- | --- | --- | --- |
| `pvp` | `true` / `false` | `false` | Allow PvP inside the region |
| `build` | `true` / `false` | `false` | Allow non-members to build |
| `interact` | `true` / `false` | `false` | Allow non-members to interact (chests, buttons…) |
| `mob-spawning` | `true` / `false` | `true` | Allow mobs to spawn |
| `explosions` | `true` / `false` | `false` | Allow TNT / creeper explosions |
| `fire` | `true` / `false` | `false` | Allow fire spread |
| `greeting` | `<text>` | — | Message shown when entering the region |
| `farewell` | `<text>` | — | Message shown when leaving the region |

```bash
# Example: enable PvP in an arena region
/region setflag my-arena pvp true
/region setflag my-arena greeting "&cYou entered a PvP zone!"
```

---

## Configuration (`protections/config.yml`)

```yaml
selection-wand: GOLDEN_AXE     # Item used to select region corners

max-regions-per-player: 5      # Max regions per player
max-region-volume: 100000      # Max region size in blocks

pvp-in-wilderness: true        # Allow PvP outside any region

duel-request-timeout-seconds: 30

economy:
  enabled: false               # Charge players to claim regions
  base-cost: 100.0             # Flat fee per claim
  cost-per-block: 0.01         # Additional cost × region volume
  refund-percent: 50           # % refunded when a region is deleted
```

---

## Duel System

The duel system lets players challenge each other to a 1v1 fight in a safe duel arena. Deaths during duels do not drop items.

### Duel Commands

| Command | Usage | Permission |
| --- | --- | --- |
| `/duel <player>` | Challenge a player to a duel | `nexusslime.duel.use` |
| `/duel accept` | Accept a duel challenge | `nexusslime.duel.use` |
| `/duel deny` | Deny a duel challenge | `nexusslime.duel.use` |
| `/duel spectate <player>` | Spectate a duel | `nexusslime.duel.use` |
| `/duel stats` | View your duel stats | `nexusslime.duel.use` |
| `/duel setarena` | Set duel arena at your location | `nexusslime.protect.admin` |

### Duel Rules

- Duel requests expire after `duel-request-timeout-seconds` (default: 30)
- Items are saved and restored after the duel ends
- The winner receives configurable rewards (set in the economy bridge)
- Both players are teleported to the duel arena on accept

---

## Permissions

| Permission | Description | Default |
| --- | --- | --- |
| `nexusslime.region.use` | Create and manage own regions | true |
| `nexusslime.protect.admin` | Admin region management | OP |
| `nexusslime.bypass.protection` | Bypass all region protections | OP |
| `nexusslime.duel.use` | Challenge and accept duels | true |

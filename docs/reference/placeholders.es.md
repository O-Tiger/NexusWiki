# Referencia PlaceholderAPI

NexusSlime registra su propia expansión PlaceholderAPI bajo el identificador `nexusslime`. Todos los placeholders siguen el patrón `%nexusslime_<nombre>%`.

**Requiere:** [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) (dependencia suave — instálalo por separado)

---

## Economía

| Placeholder | Descripción | Ejemplo |
| --- | --- | --- |
| `%nexusslime_money%` | Saldo de dinero actual del jugador | `12500.00` |
| `%nexusslime_credits%` | Saldo de créditos del jugador | `350` |

---

## Esenciales

| Placeholder | Descripción | Ejemplo |
| --- | --- | --- |
| `%nexusslime_playtime%` | Tiempo total de juego (formateado) | `3d 12h 45m` |
| `%nexusslime_playtime_minutes%` | Tiempo total de juego en minutos | `5085` |
| `%nexusslime_homes%` | Número de homes establecidos | `3` |
| `%nexusslime_afk%` | `true` si el jugador está AFK | `false` |
| `%nexusslime_afk_status%` | Estado AFK legible por humanos | `AFK` / `Online` |

---

## Clanes

| Placeholder | Descripción | Ejemplo |
| --- | --- | --- |
| `%nexusslime_clan_name%` | Nombre del clan del jugador | `Shadowborn` |
| `%nexusslime_clan_tag%` | Etiqueta del clan | `SHD` |
| `%nexusslime_clan_role%` | Rol del jugador en el clan | `Owner` / `Officer` / `Member` |
| `%nexusslime_clan_level%` | Nivel actual del clan | `5` |
| `%nexusslime_clan_members%` | Conteo de miembros en línea | `8` |
| `%nexusslime_clan_bank%` | Saldo del banco del clan | `75000.00` |

Devuelve cadena vacía si el jugador no está en un clan.

---

## Crystal Defense

| Placeholder | Descripción | Ejemplo |
| --- | --- | --- |
| `%nexusslime_crystal_wave%` | Número de oleada actual | `7` |
| `%nexusslime_crystal_health%` | HP restante del cristal | `680.0` |
| `%nexusslime_crystal_points%` | Puntos de eliminación del jugador en el juego actual | `145` |
| `%nexusslime_crystal_arena%` | Nombre de la arena en la que se encuentra el jugador | `arena1` |

Devuelve cadena vacía si el jugador no está en un juego de Crystal Defense.

---

## Seguridad

| Placeholder | Descripción | Ejemplo |
| --- | --- | --- |
| `%nexusslime_authenticated%` | `true` si el jugador está autenticado | `true` |
| `%nexusslime_auth_status%` | Estado de autenticación legible | `Authenticated` / `Pending` |

---

## Votifier

| Placeholder | Descripción | Ejemplo |
| --- | --- | --- |
| `%nexusslime_votes_total%` | Total de votos acumulados | `127` |
| `%nexusslime_vote_streak%` | Longitud de la racha de votos actual | `12` |

---

## Estadísticas del Jugador

| Placeholder | Descripción | Ejemplo |
| --- | --- | --- |
| `%nexusslime_player_blocks_broken%` | Total de bloques rotos | `48320` |
| `%nexusslime_player_machines_placed%` | Total de máquinas colocadas | `214` |
| `%nexusslime_player_items_crafted%` | Total de ítems crafteados | `5630` |
| `%nexusslime_player_energy_generated%` | Total de energía generada (RF) | `1200000` |
| `%nexusslime_player_items_smelted%` | Total de ítems fundidos | `890` |
| `%nexusslime_player_research_unlocked%` | Entradas de investigación desbloqueadas | `34` |
| `%nexusslime_player_level%` | Nivel NexusSlime del jugador | `15` |
| `%nexusslime_researched_<id>%` | `true` si una investigación específica está desbloqueada | `true` |

---

## Mochilas

| Placeholder | Descripción | Ejemplo |
| --- | --- | --- |
| `%nexusslime_backpacks_owned%` | Número de mochilas que posee el jugador | `2` |

---

## Máquinas

| Placeholder | Descripción | Ejemplo |
| --- | --- | --- |
| `%nexusslime_machines_count%` | Total de máquinas colocadas por el jugador | `42` |

---

## LuckPerms

| Placeholder | Descripción | Ejemplo |
| --- | --- | --- |
| `%nexusslime_lp_prefix%` | Prefijo LuckPerms del jugador | `&6[VIP]` |
| `%nexusslime_lp_suffix%` | Sufijo LuckPerms del jugador | `&7✦` |

Requieren que LuckPerms esté instalado.

---

## Guía

| Placeholder | Descripción |
| --- | --- |
| `%nexusslime_guide_<id>%` | Entrada dinámica de la guía para ID de ítem/máquina |

Son dinámicos — reemplaza `<id>` con cualquier ID de ítem o máquina registrado.

---

## Core / Varios

| Placeholder | Descripción | Ejemplo |
| --- | --- | --- |
| `%nexusslime_version%` | Cadena de versión del plugin | `2.0.0-BETA` |
| `%nexusslime_player%` | Nombre de usuario del jugador | `Steve` |
| `%nexusslime_uuid%` | UUID del jugador | `069a79f4-...` |

---

## Uso en Scoreboards / TAB

```yaml
# Ejemplo con el plugin TAB
header: "&bNexusSlime &7%nexusslime_version%"
tablist-name: "%nexusslime_lp_prefix%%player_name%"
scoreboard:
  title: "&b&lTus Estadísticas"
  lines:
    - "&7Dinero: &a$%nexusslime_money%"
    - "&7Créditos: &b%nexusslime_credits%"
    - "&7Votos: &e%nexusslime_votes_total% &7(racha: %nexusslime_vote_streak%)"
    - "&7Clan: &f%nexusslime_clan_name%"
    - "&7Tiempo de Juego: &f%nexusslime_playtime%"
```

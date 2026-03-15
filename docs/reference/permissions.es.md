# Referencia de Permisos

Lista completa de todos los nodos de permisos registrados por NexusSlime. Los nodos marcados como **OP** son por defecto solo para operadores; los nodos marcados como **true** se otorgan a todos los jugadores por defecto.

---

## Core & Admin

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.*` | Todos los permisos | OP |
| `nexusslime.command` | Usar el comando básico `/nexusslime` | true |
| `nexusslime.admin` | Acceso administrativo general | OP |
| `nexusslime.admin.*` | Todos los permisos administrativos | OP |
| `nexusslime.admin.reload` | Recargar configuraciones del plugin | OP |
| `nexusslime.admin.give` | Dar ítems personalizados | OP |
| `nexusslime.admin.debug` | Alternar modo de depuración | OP |
| `nexusslime.admin.cleardata` | Limpiar datos de jugadores | OP |
| `nexusslime.bypass.protection` | Ignorar todas las protecciones de región | OP |

---

## Investigación

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.research` | Acceder al sistema de investigación | true |
| `nexusslime.research.all` | Desbloquear toda la investigación instantáneamente | OP |

---

## Mochilas

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.backpack.create` | Crear mochilas | true |
| `nexusslime.backpack.upgrade` | Actualizar mochilas | true |
| `nexusslime.backpack.unlimited` | Ranuras ilimitadas de mochila | OP |

---

## Puntos de Viaje

| Permiso | Ranuras | Por defecto |
| --- | --- | --- |
| `nexusslime.essentials.waypoints.1` | 1 punto de viaje | true |
| `nexusslime.essentials.waypoints.5` | 5 puntos de viaje | — |
| `nexusslime.essentials.waypoints.25` | 25 puntos de viaje | — |
| `nexusslime.essentials.waypoints.unlimited` | Ilimitado | OP |
| `nexusslime.essentials.waypoint` | Acceder a comandos de punto de viaje | true |

---

## Homes

| Permiso | Ranuras | Por defecto |
| --- | --- | --- |
| `nexusslime.essentials.homes.1` | 1 home | true |
| `nexusslime.essentials.homes.3` | 3 homes | — |
| `nexusslime.essentials.homes.10` | 10 homes | — |
| `nexusslime.essentials.homes.unlimited` | Ilimitado | OP |
| `nexusslime.essentials.home` | Usar /home, /sethome, /delhome | true |

---

## Comandos Esenciales

| Permiso | Comando | Por defecto |
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
| `nexusslime.essentials.fly` | `/fly` (propio) | false |
| `nexusslime.essentials.fly.others` | `/fly <jugador>` | OP |
| `nexusslime.essentials.hat` | `/hat` | false |
| `nexusslime.essentials.god` | `/god` (propio) | OP |
| `nexusslime.essentials.god.others` | `/god <jugador>` | OP |
| `nexusslime.essentials.heal` | `/heal` (propio) | OP |
| `nexusslime.essentials.heal.others` | `/heal <jugador>` | OP |
| `nexusslime.essentials.feed` | `/feed` (propio) | OP |
| `nexusslime.essentials.feed.others` | `/feed <jugador>` | OP |
| `nexusslime.essentials.nick` | `/nick` (propio) | false |
| `nexusslime.essentials.nick.others` | `/nick <jugador>` | OP |
| `nexusslime.essentials.afk` | `/afk` | true |
| `nexusslime.essentials.workbench` | `/workbench` | true |
| `nexusslime.essentials.trash` | `/trash` | true |
| `nexusslime.essentials.anvil` | `/anvil` | OP |
| `nexusslime.essentials.grindstone` | `/grindstone` | OP |
| `nexusslime.essentials.stonecutter` | `/stonecutter` | OP |
| `nexusslime.essentials.speed` | `/speed` | OP |
| `nexusslime.essentials.seen` | `/seen` | true |
| `nexusslime.essentials.clearinventory` | `/clearinventory` (propio) | OP |
| `nexusslime.essentials.clearinventory.others` | `/clearinventory <jugador>` | OP |
| `nexusslime.essentials.getpos` | `/getpos` | true |
| `nexusslime.essentials.playtime` | `/playtime` | true |
| `nexusslime.essentials.gamemode` | `/gamemode` | OP |
| `nexusslime.essentials.enderchest` | `/enderchest` (propio) | true |
| `nexusslime.essentials.enderchest.others` | `/enderchest <jugador>` | OP |
| `nexusslime.essentials.repair` | `/repair` | OP |
| `nexusslime.essentials.ext` | `/ext` | OP |
| `nexusslime.essentials.exp` | `/exp` | OP |
| `nexusslime.essentials.worth` | `/worth` | true |
| `nexusslime.essentials.rules` | `/rules` | true |
| `nexusslime.essentials.skull` | `/skull` | OP |
| `nexusslime.essentials.jail.admin` | Gestión de prisión | OP |
| `nexusslime.essentials.backpack` | Comandos de mochila | true |

---

## Economía

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.economy.money` | Ver saldo de dinero | true |
| `nexusslime.economy.credits` | Ver créditos | true |
| `nexusslime.economy.baltop` | Ver tabla de clasificación | true |
| `nexusslime.economy.sell` | Usar /sell | true |
| `nexusslime.economy.admin` | Comandos administrativos de economía | OP |

---

## Clanes

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.clan.use` | Usar comandos de clan | true |
| `nexusslime.clan.admin` | Gestión administrativa de clanes | OP |
| `nexusslime.clan.bypass-protection` | Ignorar territorio de clan | OP |

---

## Seguridad

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.security.cleanworld` | Limpiador de mundo manual | OP |
| `nexusslime.staff.vanish` | Hacerse invisible | OP |
| `nexusslime.staff.vanish.others` | Hacer invisible a otro jugador | OP |
| `nexusslime.staff.vanish.see` | Ver jugadores invisibles | OP |
| `nexusslime.staff.invsee` | Inspeccionar inventarios | OP |
| `nexusslime.staff.spy` | Modo espía de chat | OP |

---

## Chat

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.chat.staff` | Acceder al canal de chat del staff | OP |
| `nexusslime.chat.mute` | Silenciar jugadores | OP |
| `nexusslime.chat.mute.bypass` | Ignorar silenciamiento | false |
| `nexusslime.chat.filter.bypass` | Ignorar filtro de palabras | OP |
| `nexusslime.chat.reload` | Recargar configuración de chat | OP |
| `nexusslime.chat.color` | Usar códigos de color en el chat | OP |

---

## Protecciones & Duelos

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.region.use` | Crear y gestionar propias regiones | true |
| `nexusslime.protect.admin` | Gestión administrativa de regiones | OP |
| `nexusslime.duel.use` | Enviar y aceptar duelos | true |

---

## Crystal Defense

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.crystaldefense.use` | Unirse a arenas | true |
| `nexusslime.crystaldefense.admin` | Crear/gestionar arenas | OP |

---

## Votifier

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.vote` | Usar `/vote` | true |
| `nexusslime.vote.top` | Usar `/votetop` | true |

---

## Custom Mobs

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.boss.admin` | Todos los comandos de boss/huevo de aparición | OP |

---

## Dreams

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.dreams.admin` | Comandos administrativos de sueños | OP |

---

## Twitch

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.twitch.use` | Comandos básicos de Twitch | true |
| `nexusslime.twitch.staff` | Aprobar vinculaciones, realizar sorteos | OP |
| `nexusslime.twitch.admin` | Recargar configuración de Twitch | OP |

---

## Silk Spawners

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.silkspawner.use` | Minar spawners con Silk Touch | true |
| `nexusslime.silkspawner.admin` | Comandos administrativos de spawner | OP |

---

## Recetas & Kits

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.recipe` | Usar `/recipe` | true |
| `nexusslime.command.kit` | Usar `/kit` | true |
| `nexusslime.command.vip` | Usar `/vip` | true |
| `nexusslime.kit.*` | Acceder a todos los kits VIP | OP |

---

## Nodos de Nivel de Permiso

Usados internamente para mapear rangos del staff. Configura en `config.yml`:

| Permiso | Rango |
| --- | --- |
| `nexusslime.level.user` | Jugador regular |
| `nexusslime.level.helper` | Asistente |
| `nexusslime.level.moderator` | Moderador |
| `nexusslime.level.admin` | Administrador |
| `nexusslime.level.owner` | Propietario |

# Referencia de Comandos

Lista completa de todos los comandos registrados por NexusSlime, organizados por módulo.

**Leyenda:**

- `<arg>` — argumento requerido
- `[arg]` — argumento opcional
- `(OP)` — solo operadores por defecto
- `(true)` — disponible para todos los jugadores por defecto

---

## Core / Plugin

| Comando | Alias | Descripción | Permiso |
| --- | --- | --- | --- |
| `/nexusslime help` | `/ns`, `/nexus`, `/slime` | Mostrar ayuda | `nexusslime.command` |
| `/nexusslime info` | | Versión y estado del plugin | `nexusslime.command` |
| `/nexusslime reload` | | Recargar todas las configuraciones | `nexusslime.admin.reload` |
| `/nexusslime give <player> <item>` | | Dar un ítem personalizado | `nexusslime.admin.give` |
| `/nexusslime guide` | | Abrir GUI de la guía de ítems | `nexusslime.command` |
| `/nexusslime modules` | | Listar todos los módulos cargados | `nexusslime.command` |
| `/nexusslime machine info <id>` | | Detalles de la máquina | `nexusslime.command` |
| `/nexusslime machine list` | | Listar todas las máquinas | `nexusslime.command` |
| `/nexusslime energy info <x,y,z>` | | Información del nodo de energía | `nexusslime.command` |
| `/nexusslime energy network` | | Ver red de energía | `nexusslime.command` |
| `/research` | | Ver progreso de investigación | `nexusslime.research` |
| `/research list [tier]` | | Listar investigaciones por tier | `nexusslime.research` |
| `/research <item-id>` | | Verificar investigación específica | `nexusslime.research` |
| `/recipe <item>` | | Mostrar receta(s) de crafteo | `nexusslime.recipe` |

---

## Mochilas & Puntos de Viaje

| Comando | Alias | Descripción | Permiso |
| --- | --- | --- | --- |
| `/backpack open [id]` | | Abrir tu mochila | `nexusslime.essentials.backpack` |
| `/backpack list` | | Listar todas las mochilas | `nexusslime.essentials.backpack` |
| `/waypoint create <name>` | `/wp` | Crear un punto de viaje | `nexusslime.essentials.waypoint` |
| `/waypoint delete <name>` | `/wp` | Eliminar un punto de viaje | `nexusslime.essentials.waypoint` |
| `/waypoint list` | `/wp` | Listar todos los puntos de viaje | `nexusslime.essentials.waypoint` |
| `/waypoint tp <name>` | `/wp` | Teletransportarse a punto de viaje | `nexusslime.essentials.waypoint` |
| `/waypoint info <name>` | `/wp` | Información del punto de viaje | `nexusslime.essentials.waypoint` |

---

## Esenciales — Homes

| Comando | Descripción | Permiso |
| --- | --- | --- |
| `/home [name]` | Teletransportarse a un home | `nexusslime.essentials.home` |
| `/home list` | Listar todos los homes | `nexusslime.essentials.home` |
| `/sethome <name>` | Establecer home en la ubicación actual | `nexusslime.essentials.home` |
| `/delhome <name>` | Eliminar un home | `nexusslime.essentials.home` |

---

## Esenciales — Warps

| Comando | Descripción | Permiso |
| --- | --- | --- |
| `/warp <name>` | Teletransportarse a un warp | `nexusslime.essentials.warp.use` |
| `/warp list` | Listar todos los warps | `nexusslime.essentials.warp.use` |
| `/setwarp <name>` | Crear un warp (OP) | `nexusslime.essentials.warp.admin` |
| `/delwarp <name>` | Eliminar un warp (OP) | `nexusslime.essentials.warp.admin` |

---

## Esenciales — Teletransporte

| Comando | Descripción | Permiso |
| --- | --- | --- |
| `/tpa <player>` | Enviar solicitud de teletransporte | `nexusslime.essentials.tpa` |
| `/tpaccept` | Aceptar solicitud de teletransporte | `nexusslime.essentials.tpa` |
| `/tpdeny` | Rechazar solicitud de teletransporte | `nexusslime.essentials.tpa` |
| `/tphere <player>` | Convocar un jugador (OP) | `nexusslime.essentials.tphere` |
| `/tppos <x> <y> <z>` | Teletransportarse a coordenadas (OP) | `nexusslime.essentials.tppos` |
| `/spawn` | Teletransportarse al spawn | `nexusslime.essentials.spawn` |
| `/setspawn` | Establecer spawn del servidor (OP) | `nexusslime.essentials.setspawn` |
| `/back` | Regresar a la ubicación anterior | `nexusslime.essentials.back` |

---

## Esenciales — Utilidades

| Comando | Descripción | Permiso |
| --- | --- | --- |
| `/afk` | Alternar AFK | `nexusslime.essentials.afk` |
| `/fly` | Alternar vuelo (propio) | `nexusslime.essentials.fly` |
| `/fly <player>` | Alternar vuelo (otro, OP) | `nexusslime.essentials.fly.others` |
| `/god` | Alternar modo dios | `nexusslime.essentials.god` |
| `/god <player>` | Alternar dios (otro, OP) | `nexusslime.essentials.god.others` |
| `/heal` | Curarse a sí mismo (OP) | `nexusslime.essentials.heal` |
| `/heal <player>` | Curar a otro (OP) | `nexusslime.essentials.heal.others` |
| `/feed` | Alimentarse a sí mismo (OP) | `nexusslime.essentials.feed` |
| `/feed <player>` | Alimentar a otro (OP) | `nexusslime.essentials.feed.others` |
| `/nick <name>` | Establecer apodo | `nexusslime.essentials.nick` |
| `/nick <player> <name>` | Establecer apodo (otro, OP) | `nexusslime.essentials.nick.others` |
| `/hat` | Usar ítem como sombrero | `nexusslime.essentials.hat` |
| `/speed <value>` | Establecer velocidad de caminar/volar (OP) | `nexusslime.essentials.speed` |
| `/workbench` | Banco de trabajo portátil | `nexusslime.essentials.workbench` |
| `/anvil` | Yunque portátil (OP) | `nexusslime.essentials.anvil` |
| `/grindstone` | Piedra de afilar portátil (OP) | `nexusslime.essentials.grindstone` |
| `/stonecutter` | Cortadora de piedra portátil (OP) | `nexusslime.essentials.stonecutter` |
| `/trash` | Papelera portátil | `nexusslime.essentials.trash` |
| `/near` | Listar jugadores cercanos | `nexusslime.essentials.near` |
| `/seen <player>` | Información de última conexión | `nexusslime.essentials.seen` |
| `/getpos` | Mostrar coordenadas | `nexusslime.essentials.getpos` |
| `/playtime` | Verificar tiempo de juego | `nexusslime.essentials.playtime` |
| `/gamemode <mode>` | Cambiar modo de juego (OP) | `nexusslime.essentials.gamemode` |
| `/enderchest` | Abrir cofre del End | `nexusslime.essentials.enderchest` |
| `/enderchest <player>` | Abrir cofre del End de otro (OP) | `nexusslime.essentials.enderchest.others` |
| `/clearinventory` | Limpiar propio inventario (OP) | `nexusslime.essentials.clearinventory` |
| `/clearinventory <player>` | Limpiar inventario de otro (OP) | `nexusslime.essentials.clearinventory.others` |
| `/repair` | Reparar ítem en mano (OP) | `nexusslime.essentials.repair` |
| `/ext` | Apagarse a sí mismo (OP) | `nexusslime.essentials.ext` |
| `/exp <amount>` | Dar XP (OP) | `nexusslime.essentials.exp` |
| `/skull [player]` | Obtener cabeza de jugador (OP) | `nexusslime.essentials.skull` |
| `/rules` | Mostrar reglas del servidor | `nexusslime.essentials.rules` |
| `/worth [item]` | Valor de venta del ítem | `nexusslime.essentials.worth` |

---

## Esenciales — Prisión

| Comando | Descripción | Permiso |
| --- | --- | --- |
| `/jail <player> [duration]` | Encarcelar a un jugador (OP) | `nexusslime.essentials.jail.admin` |
| `/unjail <player>` | Liberar a un jugador (OP) | `nexusslime.essentials.jail.admin` |
| `/setjail` | Establecer ubicación de la prisión (OP) | `nexusslime.essentials.jail.admin` |

---

## Economía

| Comando | Descripción | Permiso |
| --- | --- | --- |
| `/money [player]` | Verificar saldo | `nexusslime.economy.money` |
| `/credits [player]` | Verificar créditos | `nexusslime.economy.credits` |
| `/baltop` | Top 10 más ricos | `nexusslime.economy.baltop` |
| `/sell hand` | Vender ítem en mano | `nexusslime.economy.sell` |
| `/sell all` | Vender todos los ítems vendibles | `nexusslime.economy.sell` |
| `/sell inventory` | Vender inventario completo | `nexusslime.economy.sell` |
| `/worth [item]` | Verificar valor de venta | `nexusslime.essentials.worth` |
| `/eco give <player> <amount>` | Dar dinero (OP) | `nexusslime.economy.admin` |
| `/eco take <player> <amount>` | Quitar dinero (OP) | `nexusslime.economy.admin` |
| `/eco set <player> <amount>` | Establecer saldo (OP) | `nexusslime.economy.admin` |
| `/eco reset <player>` | Resetear saldo (OP) | `nexusslime.economy.admin` |

---

## Clanes

| Comando | Descripción | Permiso |
| --- | --- | --- |
| `/clan create <name> <tag>` | Crear un clan | `nexusslime.clan.use` |
| `/clan disband` | Disolver clan | `nexusslime.clan.use` |
| `/clan invite <player>` | Invitar a un jugador | `nexusslime.clan.use` |
| `/clan join <name>` | Unirse a un clan | `nexusslime.clan.use` |
| `/clan leave` | Salir del clan | `nexusslime.clan.use` |
| `/clan kick <player>` | Expulsar a un miembro | `nexusslime.clan.use` |
| `/clan promote <player>` | Ascender a oficial | `nexusslime.clan.use` |
| `/clan demote <player>` | Degradar a miembro | `nexusslime.clan.use` |
| `/clan info [name]` | Información del clan | `nexusslime.clan.use` |
| `/clan list` | Listar todos los clanes | `nexusslime.clan.use` |
| `/clan chat` | Alternar chat de clan | `nexusslime.clan.use` |
| `/clan claim` | Reclamar chunk actual | `nexusslime.clan.use` |
| `/clan unclaim` | Liberar chunk actual | `nexusslime.clan.use` |
| `/clan map` | Mostrar mapa de territorio | `nexusslime.clan.use` |
| `/clan chest` | Abrir cofre del clan | `nexusslime.clan.use` |
| `/clan upgrade` | Abrir menú de mejoras | `nexusslime.clan.use` |
| `/clan top` | Clasificación de clanes | `nexusslime.clan.use` |
| `/clan admin disband <name>` | Forzar disolución (OP) | `nexusslime.clan.admin` |
| `/clan admin unclaim <name>` | Forzar liberación (OP) | `nexusslime.clan.admin` |

---

## Seguridad & Staff

| Comando | Descripción | Permiso |
| --- | --- | --- |
| `/register <password> <confirm>` | Registrar cuenta | *(todos)* |
| `/login <password>` | Iniciar sesión | *(todos)* |
| `/changepassword <old> <new>` | Cambiar contraseña | *(autenticado)* |
| `/vanish` | Alternar invisibilidad (OP) | `nexusslime.staff.vanish` |
| `/vanish <player>` | Hacer invisible a otro (OP) | `nexusslime.staff.vanish.others` |
| `/invsee <player>` | Inspeccionar inventario (OP) | `nexusslime.staff.invsee` |
| `/spy` | Alternar espía de chat (OP) | `nexusslime.staff.spy` |
| `/cleanworld` | Ejecutar limpiador de mundo (OP) | `nexusslime.security.cleanworld` |

---

## Discord

| Comando | Descripción | Permiso |
| --- | --- | --- |
| `/discord` | Enlace de invitación de Discord | *(todos)* |
| `/discord link` | Iniciar vinculación de cuenta | *(todos)* |
| `/discord unlink` | Desvincular cuenta | *(todos)* |
| `/discord info` | Mostrar cuenta vinculada | *(todos)* |
| `/discordrr` | Gestionar roles de reacción (OP) | `nexusslime.admin` |

---

## Protecciones & Duelos

| Comando | Descripción | Permiso |
| --- | --- | --- |
| `/region claim <name>` | Reclamar área seleccionada | `nexusslime.region.use` |
| `/region delete <name>` | Eliminar región | `nexusslime.region.use` |
| `/region list` | Listar tus regiones | `nexusslime.region.use` |
| `/region info [name]` | Detalles de la región | `nexusslime.region.use` |
| `/region addmember <region> <player>` | Añadir miembro | `nexusslime.region.use` |
| `/region removemember <region> <player>` | Eliminar miembro | `nexusslime.region.use` |
| `/region setflag <region> <flag> <val>` | Establecer una flag | `nexusslime.region.use` |
| `/region flags <region>` | Ver flags | `nexusslime.region.use` |
| `/protect <name>` | Protección rápida de chunk | `nexusslime.region.use` |
| `/region admin list` | Admin: todas las regiones (OP) | `nexusslime.protect.admin` |
| `/region admin delete <name>` | Admin: eliminar región (OP) | `nexusslime.protect.admin` |
| `/duel <player>` | Desafiar a duelo | `nexusslime.duel.use` |
| `/duel accept` | Aceptar duelo | `nexusslime.duel.use` |
| `/duel deny` | Rechazar duelo | `nexusslime.duel.use` |
| `/duel spectate <player>` | Espectador de duelo | `nexusslime.duel.use` |
| `/duel stats` | Estadísticas de duelo | `nexusslime.duel.use` |
| `/duel setarena` | Establecer arena de duelo (OP) | `nexusslime.protect.admin` |

---

## Crystal Defense

| Comando | Descripción | Permiso |
| --- | --- | --- |
| `/crystal join <arena>` | Unirse a una arena | `nexusslime.crystaldefense.use` |
| `/crystal leave` | Salir de la arena | `nexusslime.crystaldefense.use` |
| `/crystal list` | Listar arenas | `nexusslime.crystaldefense.use` |
| `/crystal status` | Oleada y HP del cristal | `nexusslime.crystaldefense.use` |
| `/crystal create <name>` | Crear arena (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal delete <name>` | Eliminar arena (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal setcrystal <arena>` | Establecer ubicación del cristal (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal setspawn <arena>` | Establecer spawn (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal start [arena]` | Forzar inicio (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal stop [arena]` | Detener juego (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal reload` | Recargar configuraciones (OP) | `nexusslime.crystaldefense.admin` |

---

## Votifier

| Comando | Descripción | Permiso |
| --- | --- | --- |
| `/vote` | Mostrar enlaces de votación y racha | `nexusslime.vote` |
| `/votetop` | Clasificación de votos | `nexusslime.vote.top` |

---

## Custom Mobs

| Comando | Descripción | Permiso |
| --- | --- | --- |
| `/boss spawn <id>` | Invocar un boss | `nexusslime.boss.admin` |
| `/boss spawn <id> <w> <x> <y> <z>` | Invocar en coordenadas | `nexusslime.boss.admin` |
| `/boss list` | Listar todos los bosses | `nexusslime.boss.admin` |
| `/boss info <id>` | Definición del boss | `nexusslime.boss.admin` |
| `/boss kill <id>` | Matar todas las instancias del boss | `nexusslime.boss.admin` |
| `/bossegg give <player> <id>` | Dar huevo de aparición | `nexusslime.boss.admin` |

---

## Dreams

| Comando | Descripción | Permiso |
| --- | --- | --- |
| `/dreams reload` | Recargar configuración | `nexusslime.dreams.admin` |
| `/dreams trigger <player>` | Forzar sueño | `nexusslime.dreams.admin` |
| `/dreams trigger <player> nightmare` | Forzar pesadilla | `nexusslime.dreams.admin` |

---

## Twitch

| Comando | Descripción | Permiso |
| --- | --- | --- |
| `/twitch link <username>` | Iniciar vinculación | `nexusslime.twitch.use` |
| `/twitch unlink` | Desvincular cuenta | `nexusslime.twitch.use` |
| `/twitch status` | Estado de vinculación | `nexusslime.twitch.use` |
| `/twitch approve <player>` | Aprobar vinculación (OP) | `nexusslime.twitch.staff` |
| `/twitch reject <player>` | Rechazar vinculación (OP) | `nexusslime.twitch.staff` |
| `/twitch pending` | Solicitudes pendientes (OP) | `nexusslime.twitch.staff` |
| `/twitch giveaway <streamer>` | Realizar sorteo (OP) | `nexusslime.twitch.staff` |
| `/twitch reload` | Recargar configuración (OP) | `nexusslime.twitch.admin` |

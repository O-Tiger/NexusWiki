# Módulo Esenciales

El módulo Esenciales proporciona **+40 comandos de calidad de vida** que cubren homes, warps, waypoints, teletransporte, detección de AFK, cárcel y comandos utilitarios del día a día.

---

## Homes

Los jugadores pueden establecer homes con nombre y teletransportarse a ellas.

### Comandos

| Comando | Uso | Permiso |
| --- | --- | --- |
| `/home [nombre]` | Teletransportarse a una home | `nexusslime.essentials.home` |
| `/home list` | Listar todas las homes | `nexusslime.essentials.home` |
| `/sethome <nombre>` | Establecer home en la posición actual | `nexusslime.essentials.home` |
| `/delhome <nombre>` | Eliminar una home | `nexusslime.essentials.home` |

### Permisos de Slots de Home

| Permiso | Slots |
| --- | --- |
| `nexusslime.essentials.homes.1` | 1 (predeterminado) |
| `nexusslime.essentials.homes.3` | 3 |
| `nexusslime.essentials.homes.10` | 10 |
| `nexusslime.essentials.homes.unlimited` | Ilimitado (OP) |

---

## Warps

Destinos de teletransporte públicos en todo el servidor gestionados por admins.

### Comandos de Warps

| Comando | Uso | Permiso |
| --- | --- | --- |
| `/warp <nombre>` | Teletransportarse a un warp | `nexusslime.essentials.warp.use` |
| `/warp list` | Listar todos los warps | `nexusslime.essentials.warp.use` |
| `/setwarp <nombre>` | Crear un warp (OP) | `nexusslime.essentials.warp.admin` |
| `/delwarp <nombre>` | Eliminar un warp (OP) | `nexusslime.essentials.warp.admin` |

---

## TPA (Solicitudes de Teletransporte)

### Comandos TPA

| Comando | Uso | Permiso |
| --- | --- | --- |
| `/tpa <jugador>` | Enviar solicitud de teletransporte | `nexusslime.essentials.tpa` |
| `/tpaccept` | Aceptar solicitud de teletransporte | `nexusslime.essentials.tpa` |
| `/tpdeny` | Rechazar solicitud de teletransporte | `nexusslime.essentials.tpa` |
| `/tphere <jugador>` | Teletransportar jugador hasta ti (OP) | `nexusslime.essentials.tphere` |
| `/tppos <x> <y> <z>` | Teletransportarse a coordenadas (OP) | `nexusslime.essentials.tppos` |
| `/spawn` | Teletransportarse al spawn | `nexusslime.essentials.spawn` |
| `/setspawn` | Establecer el spawn del servidor (OP) | `nexusslime.essentials.setspawn` |
| `/back` | Volver a la ubicación anterior | `nexusslime.essentials.back` |

### Configuración (`essentials/config.yml`)

```yaml
tpa:
  expiry-seconds: 60       # La solicitud expira tras este tiempo

back:
  save-on-death: true      # Guardar ubicación de muerte para /back
  save-on-any-teleport: false

spawn:
  respawn-at-spawn: false  # Forzar respawn en el spawn (vs. cama)
```

---

## Sistema AFK

### Comandos AFK

| Comando | Uso | Permiso |
| --- | --- | --- |
| `/afk` | Alternar estado AFK | `nexusslime.essentials.afk` |

### Configuración AFK

```yaml
afk:
  idle-seconds: 300        # AFK automático tras 5 minutos inactivo
  broadcast: true          # Anunciar cuando un jugador entra en AFK
```

---

## Cárcel

Los admins pueden enviar jugadores a una ubicación de cárcel predefinida.

### Comandos de Cárcel

| Comando | Uso | Permiso |
| --- | --- | --- |
| `/jail <jugador> [duración]` | Encarcelar a un jugador (OP) | `nexusslime.essentials.jail.admin` |
| `/unjail <jugador>` | Liberar a un jugador (OP) | `nexusslime.essentials.jail.admin` |
| `/setjail` | Establecer ubicación de la cárcel (OP) | `nexusslime.essentials.jail.admin` |

---

## Comandos Utilitarios

| Comando | Uso | Permiso |
| --- | --- | --- |
| `/fly` | Alternar modo vuelo | `nexusslime.essentials.fly` |
| `/fly <jugador>` | Alternar vuelo para otro jugador (OP) | `nexusslime.essentials.fly.others` |
| `/god` | Alternar modo dios | `nexusslime.essentials.god` |
| `/heal` | Curarte a ti mismo (OP) | `nexusslime.essentials.heal` |
| `/feed` | Alimentarte a ti mismo (OP) | `nexusslime.essentials.feed` |
| `/nick <nombre>` | Establecer apodo | `nexusslime.essentials.nick` |
| `/workbench` | Mesa de trabajo portátil | `nexusslime.essentials.workbench` |
| `/trash` | Papelera portátil | `nexusslime.essentials.trash` |
| `/anvil` | Yunque portátil (OP) | `nexusslime.essentials.anvil` |
| `/speed <valor>` | Establecer velocidad de movimiento (OP) | `nexusslime.essentials.speed` |
| `/near` | Listar jugadores cercanos | `nexusslime.essentials.near` |
| `/seen <jugador>` | Última vez visto | `nexusslime.essentials.seen` |
| `/getpos` | Mostrar tus coordenadas | `nexusslime.essentials.getpos` |
| `/playtime` | Verificar tiempo de juego | `nexusslime.essentials.playtime` |
| `/gamemode <modo>` | Cambiar modo de juego (OP) | `nexusslime.essentials.gamemode` |
| `/enderchest` | Abrir tu cofre de ender | `nexusslime.essentials.enderchest` |
| `/repair` | Reparar el ítem sostenido (OP) | `nexusslime.essentials.repair` |
| `/ext` | Apagarte a ti mismo (OP) | `nexusslime.essentials.ext` |
| `/hat` | Usar ítem como sombrero | `nexusslime.essentials.hat` |
| `/rules` | Mostrar reglas del servidor | `nexusslime.essentials.rules` |
| `/worth [ítem]` | Verificar valor de venta | `nexusslime.essentials.worth` |

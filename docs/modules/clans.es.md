# Módulo Clanes

El módulo Clanes permite que los jugadores creen equipos persistentes con **conquista de territorio**, **árbol de mejoras**, un **cofre compartido** y **chat de clan**.

---

## Comandos

| Comando | Uso | Permiso |
| --- | --- | --- |
| `/clan create <nombre> <tag>` | Crear un nuevo clan | `nexusslime.clan.use` |
| `/clan disband` | Disolver el clan | `nexusslime.clan.use` |
| `/clan invite <jugador>` | Invitar a un jugador | `nexusslime.clan.use` |
| `/clan join <nombre>` | Unirse a un clan | `nexusslime.clan.use` |
| `/clan leave` | Abandonar el clan | `nexusslime.clan.use` |
| `/clan kick <jugador>` | Expulsar a un miembro | `nexusslime.clan.use` |
| `/clan promote <jugador>` | Promover a oficial | `nexusslime.clan.use` |
| `/clan demote <jugador>` | Degradar a miembro | `nexusslime.clan.use` |
| `/clan info [nombre]` | Ver información del clan | `nexusslime.clan.use` |
| `/clan list` | Listar todos los clanes | `nexusslime.clan.use` |
| `/clan chat` | Alternar chat de clan | `nexusslime.clan.use` |
| `/clan claim` | Reclamar chunk actual | `nexusslime.clan.use` |
| `/clan unclaim` | Liberar chunk actual | `nexusslime.clan.use` |
| `/clan map` | Mostrar mapa de territorio | `nexusslime.clan.use` |
| `/clan chest` | Abrir cofre del clan | `nexusslime.clan.use` |
| `/clan upgrade` | Abrir menú de mejoras | `nexusslime.clan.use` |
| `/clan top` | Clasificación de clanes | `nexusslime.clan.use` |
| `/clan admin disband <nombre>` | Forzar disolución (admin) | `nexusslime.clan.admin` |

---

## Roles

| Rol | Permisos |
| --- | --- |
| **Líder** | Todas las acciones, disolver, mejorar |
| **Oficial** | Invitar, expulsar miembros, gestionar territorio |
| **Miembro** | Acceder al cofre, chat, usar territorio |

---

## Sistema de Territorio

Los clanes reclaman chunks como territorio. Los miembros pueden construir libremente; los no-miembros son bloqueados (cuando la protección está activada).

### Configuración (`clans/config.yml`)

```yaml
pvp-friendly-fire: false       # Los miembros no pueden atacarse entre sí

clan-name-min-length: 3
clan-name-max-length: 16
clan-tag-min-length: 2
clan-tag-max-length: 4

base-member-cap: 10            # Miembros en nivel 1
base-territory-cap: 10         # Chunks reclamables en nivel 1

neutral-chunk-protection: false

territory-worlds:
  - world
  - world_nether
```

---

## Árbol de Mejoras (`clans/upgrades.yml`)

```yaml
upgrades:
  member_cap:
    display-name: "&aExpansión de Miembros"
    description: "Aumenta el máximo de miembros en 5."
    max-level: 5
    cost-per-level:
      money: 5000
    bonus-per-level:
      members: 5

  territory_cap:
    display-name: "&aExpansión de Territorio"
    description: "Reclama 10 chunks adicionales por nivel."
    max-level: 10
    cost-per-level:
      money: 3000
    bonus-per-level:
      chunks: 10
```

---

## Permisos

| Permiso | Descripción | Predeterminado |
| --- | --- | --- |
| `nexusslime.clan.use` | Usar comandos de clan | true |
| `nexusslime.clan.admin` | Gestión admin de clanes | OP |
| `nexusslime.clan.bypass-protection` | Ignorar protección de territorio | OP |

---

## PlaceholderAPI

| Placeholder | Descripción |
| --- | --- |
| `%nexusslime_clan_name%` | Nombre del clan del jugador |
| `%nexusslime_clan_tag%` | Tag del clan |
| `%nexusslime_clan_role%` | Rol del jugador en el clan |
| `%nexusslime_clan_level%` | Nivel del clan |
| `%nexusslime_clan_members%` | Conteo de miembros en línea |
| `%nexusslime_clan_bank%` | Saldo del banco del clan |

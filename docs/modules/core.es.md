# Módulo Core

El módulo Core es la base de NexusSlime. Gestiona el registro de ítems personalizados, el sistema de etiquetado PDC (PersistentDataContainer), el motor de máquinas, el árbol de investigación, mochilas y puntos de viaje.

---

## Sistema de Ítems Personalizados

Todos los ítems personalizados se definen en `plugins/NexusSlime/items.yml`. El plugin incluye **más de 235 ítems** de fábrica.

### Ejemplo de `items.yml`

```yaml
COPPER_DUST:
  category: DUST
  tier: BASIC
  display-name: "&fCopper Dust"
  lore:
    - "&7A fine copper powder."
  material: PAPER
  custom-model-data: 1001
  glow: false
  stackable: true
  max-stack: 64

NEXUS_PICKAXE:
  category: TOOL
  tier: ADVANCED
  display-name: "&bNexus Pickaxe"
  lore:
    - "&7Mines at incredible speed."
    - "&8Tier: Advanced"
  material: DIAMOND_PICKAXE
  custom-model-data: 2005
  glow: true
  enchantments:
    EFFICIENCY: 5
    UNBREAKING: 3
```

### Categorías de Ítems

| Categoría | Descripción |
| --- | --- |
| `DUST` | Polvos de crafteo (cobre, estaño, plata…) |
| `INGOT` | Lingotes de metal procesados |
| `TOOL` | Herramientas y armas personalizadas |
| `MACHINE` | Bloques de máquina colocables |
| `COMPONENT` | Placas de circuito, engranajes, etc. |
| `RESOURCE` | Recursos crudos de crafteo |
| `ENERGY` | Componentes de energía |
| `BACKPACK` | Ítems de mochila |

### Tiers de Ítems (`NexusTier`)

| Tier | Descripción |
| --- | --- |
| `BASIC` | Tier inicial — sin investigación requerida |
| `ADVANCED` | Requiere investigación básica |
| `INFINITY` | Tier final — requiere pergaminos |

---

## Sistema PDC

NexusSlime usa el **PersistentDataContainer** de Minecraft para etiquetar ítems personalizados, máquinas y datos de jugadores. Cada ítem de NexusSlime lleva una clave PDC `nexusslime:id` que lo identifica de forma única.

Clases principales:

- `CustomItemRegistry` — registra y resuelve todos los ítems personalizados
- `NexusItemIdResolver` — resuelve IDs de ítems desde PDC
- `NexusItemMigrator` — migra ítems legados a nuevos IDs

---

## Sistema de Investigación

Los jugadores desbloquean ítems y máquinas gastando XP en investigación. La investigación está escalonada — **Básica → Avanzada → Infinity**.

```yaml
# researches.yml
COPPER_PROCESSING:
  tier: BASIC
  xp-cost: 10
  display-name: "&fCopper Processing"
  description: "Unlock copper dust, copper ingots, and basic machines."
  unlocks:
    - COPPER_DUST
    - COPPER_INGOT
    - BASIC_CRUSHER
```

| Permiso | Descripción |
| --- | --- |
| `nexusslime.research` | Usar el sistema de investigación (por defecto: true) |
| `nexusslime.research.all` | Desbloquear toda la investigación instantáneamente (OP) |

---

## Mochilas

Las mochilas son contenedores de almacenamiento portátiles. Los jugadores comienzan con una mochila básica y pueden actualizarla.

### Comandos

| Comando | Uso | Permiso |
| --- | --- | --- |
| `/backpack open` | Abrir tu mochila | `nexusslime.essentials.backpack` |
| `/backpack open <id>` | Abrir una mochila específica | `nexusslime.essentials.backpack` |
| `/backpack list` | Listar todas las mochilas | `nexusslime.essentials.backpack` |

### Permisos

| Permiso | Descripción |
| --- | --- |
| `nexusslime.backpack.create` | Crear mochilas (por defecto: true) |
| `nexusslime.backpack.upgrade` | Actualizar mochilas (por defecto: true) |
| `nexusslime.backpack.unlimited` | Ranuras ilimitadas de mochila (OP) |

---

## Puntos de Viaje

Los puntos de viaje son puntos de viaje rápido personales guardados por el jugador.

### Comandos de Puntos de Viaje

| Comando | Uso | Permiso |
| --- | --- | --- |
| `/waypoint create <nombre>` | Crear un punto de viaje | `nexusslime.essentials.waypoint` |
| `/waypoint delete <nombre>` | Eliminar un punto de viaje | `nexusslime.essentials.waypoint` |
| `/waypoint list` | Listar todos los puntos de viaje | `nexusslime.essentials.waypoint` |
| `/waypoint tp <nombre>` | Teletransportarse a un punto de viaje | `nexusslime.essentials.waypoint` |
| `/waypoint info <nombre>` | Mostrar detalles del punto de viaje | `nexusslime.essentials.waypoint` |

Alias: `/wp`

### Permisos de Límite de Ranuras

| Permiso | Ranuras |
| --- | --- |
| `nexusslime.essentials.waypoints.1` | 1 (por defecto) |
| `nexusslime.essentials.waypoints.5` | 5 |
| `nexusslime.essentials.waypoints.25` | 25 |
| `nexusslime.essentials.waypoints.unlimited` | Ilimitado (OP) |

---

## Comandos Principales del Plugin

| Comando | Uso | Permiso |
| --- | --- | --- |
| `/nexusslime help` | Mostrar ayuda | `nexusslime.command` |
| `/nexusslime info` | Información del plugin | `nexusslime.command` |
| `/nexusslime reload` | Recargar todas las configuraciones | `nexusslime.admin.reload` |
| `/nexusslime give <jugador> <item>` | Dar un ítem personalizado | `nexusslime.admin.give` |
| `/nexusslime guide` | Abrir la guía de ítems | `nexusslime.command` |
| `/nexusslime modules` | Listar módulos cargados | `nexusslime.command` |
| `/nexusslime machine info <id>` | Información de la máquina | `nexusslime.command` |
| `/nexusslime machine list` | Listar máquinas | `nexusslime.command` |
| `/nexusslime energy info <loc>` | Información del nodo de energía | `nexusslime.command` |
| `/nexusslime energy network` | Vista de la red de energía | `nexusslime.command` |

Alias: `/ns`, `/nexus`, `/slime`, `/nslime`

---

## Soporte de Idiomas

NexusSlime incluye cuatro archivos de idioma:

| Archivo | Idioma |
| --- | --- |
| `lang/en_US.yml` | Inglés (por defecto) |
| `lang/pt_BR.yml` | Portugués Brasileño |
| `lang/es_ES.yml` | Español |
| `lang/zh_CN.yml` | Chino (Simplificado) |

Establece el idioma activo en `config.yml`:

```yaml
settings:
  language: en_US
```

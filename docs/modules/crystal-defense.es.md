# Módulo Crystal Defense

Crystal Defense es un **minijuego cooperativo por oleadas** donde los jugadores defienden Ender Crystals contra hordas de mobs cada vez más difíciles. Los jugadores ganan puntos por cada muerte y los gastan en mejoras de arena.

---

## Cómo Jugar

1. Un administrador crea una arena con `/crystal create <nombre>`
2. Los jugadores se unen a la arena con `/crystal join <nombre>`
3. El juego comienza automáticamente cuando hay suficientes jugadores listos (o manualmente con `/crystal start`)
4. Los mobs aparecen en oleadas — elimínalos antes de que destruyan el cristal
5. Gasta los puntos de eliminación en mejoras entre oleadas
6. El juego termina cuando el HP del cristal llega a cero

---

## Comandos

| Comando | Uso | Permiso |
| --- | --- | --- |
| `/crystal join <arena>` | Unirse a una arena | `nexusslime.crystaldefense.use` |
| `/crystal leave` | Salir de la arena actual | `nexusslime.crystaldefense.use` |
| `/crystal list` | Listar arenas disponibles | `nexusslime.crystaldefense.use` |
| `/crystal status` | Mostrar oleada actual y HP del cristal | `nexusslime.crystaldefense.use` |
| `/crystal create <nombre>` | Crear una nueva arena | `nexusslime.crystaldefense.admin` |
| `/crystal delete <nombre>` | Eliminar una arena | `nexusslime.crystaldefense.admin` |
| `/crystal setcrystal <arena>` | Establecer ubicación del cristal | `nexusslime.crystaldefense.admin` |
| `/crystal setspawn <arena>` | Establecer punto de aparición de jugadores | `nexusslime.crystaldefense.admin` |
| `/crystal start [arena]` | Forzar inicio de un juego | `nexusslime.crystaldefense.admin` |
| `/crystal stop [arena]` | Detener un juego | `nexusslime.crystaldefense.admin` |
| `/crystal reload` | Recargar configuraciones de arenas | `nexusslime.crystaldefense.admin` |

---

## Configuración de Arena

1. Construye tu arena en el mundo
2. Ejecuta `/crystal create <nombre>`
3. Párate en la posición del Ender Crystal → `/crystal setcrystal <nombre>`
4. Párate en el punto de aparición de jugadores → `/crystal setspawn <nombre>`
5. (Opcional) Edita `crystaldefense/config.yml` para configurar oleadas y costos de mejoras

---

## Configuración Principal (`crystaldefense/config.yml`)

```yaml
arena:
  crystal-max-health: 1000.0    # HP por defecto del cristal para nuevas arenas

points:
  per-kill: 5                   # Puntos ganados por cada mob eliminado

upgrades:
  crystal_health:
    base_cost: 20
    step_percent: 20            # El HP máximo del cristal aumenta 20% por compra

  crystal_defense:
    base_cost: 25
    duration_seconds: 30        # Duración de RESISTANCE II aplicada a todos los jugadores

  player_attack_buff:
    base_cost: 30
    damage_percent: 20          # % de aumento en el daño base de ataque del jugador
    duration_seconds: 60
```

---

## Definición de Oleadas (`crystaldefense/waves.yml`)

```yaml
waves:
  1:
    mobs:
      - type: ZOMBIE
        count: 10
        health-multiplier: 1.0
      - type: SKELETON
        count: 5
        health-multiplier: 1.0
    delay-seconds: 3

  2:
    mobs:
      - type: ZOMBIE
        count: 15
        health-multiplier: 1.2
      - type: SKELETON
        count: 8
        health-multiplier: 1.1
      - type: CREEPER
        count: 3
        health-multiplier: 1.0
    delay-seconds: 3

  5:
    mobs:
      - type: WITHER_SKELETON
        count: 5
        health-multiplier: 1.5
      - type: BLAZE
        count: 10
        health-multiplier: 1.3
    delay-seconds: 5
    boss:
      type: WITHER
      health: 300.0
```

---

## Mejoras

| Mejora | Efecto | Costo Base |
| --- | --- | --- |
| **Crystal Health** | Aumenta el HP máximo del cristal en 20% por nivel | 20 puntos |
| **Crystal Defense** | Aplica RESISTANCE II a todos los jugadores por 30s | 25 puntos |
| **Player Attack Buff** | +20% de daño por 60s | 30 puntos |

---

## Permisos

| Permiso | Descripción | Por defecto |
| --- | --- | --- |
| `nexusslime.crystaldefense.use` | Unirse a arenas y jugar | true |
| `nexusslime.crystaldefense.admin` | Crear/gestionar arenas | OP |

---

## PlaceholderAPI

| Placeholder | Descripción |
| --- | --- |
| `%nexusslime_crystal_wave%` | Número de oleada actual |
| `%nexusslime_crystal_health%` | HP restante del cristal |
| `%nexusslime_crystal_points%` | Puntos del jugador en el juego actual |
| `%nexusslime_crystal_arena%` | Arena en la que se encuentra el jugador |

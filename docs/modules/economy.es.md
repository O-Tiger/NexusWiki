# Módulo Economía

El módulo Economía proporciona un **sistema de moneda dual** (dinero y créditos), comandos de venta, clasificación de riqueza y configuración de precios de venta por ítem.

---

## Resumen

| Moneda | Descripción |
| --- | --- |
| **Dinero** (`$`) | Moneda estándar del juego, ganada vendiendo ítems, votando, etc. |
| **Créditos** | Moneda premium, normalmente obtenida en la webstore |

---

## Comandos

| Comando | Uso | Permiso |
| --- | --- | --- |
| `/money` | Verificar tu saldo | `nexusslime.economy.money` |
| `/money <jugador>` | Verificar saldo de otro jugador | `nexusslime.economy.money` |
| `/credits` | Verificar tus créditos | `nexusslime.economy.credits` |
| `/baltop` | Top 10 jugadores más ricos | `nexusslime.economy.baltop` |
| `/sell hand` | Vender ítem en mano | `nexusslime.economy.sell` |
| `/sell all` | Vender todos los ítems vendibles | `nexusslime.economy.sell` |
| `/sell inventory` | Vender inventario completo | `nexusslime.economy.sell` |
| `/worth [ítem]` | Verificar valor de venta del ítem | `nexusslime.essentials.worth` |
| `/eco give <jugador> <cantidad>` | Dar dinero (admin) | `nexusslime.economy.admin` |
| `/eco take <jugador> <cantidad>` | Quitar dinero (admin) | `nexusslime.economy.admin` |
| `/eco set <jugador> <cantidad>` | Establecer saldo (admin) | `nexusslime.economy.admin` |
| `/eco reset <jugador>` | Resetear saldo (admin) | `nexusslime.economy.admin` |

---

## Permisos

| Permiso | Descripción | Predeterminado |
| --- | --- | --- |
| `nexusslime.economy.money` | Ver saldos | true |
| `nexusslime.economy.credits` | Ver créditos | true |
| `nexusslime.economy.baltop` | Ver clasificación | true |
| `nexusslime.economy.sell` | Usar /sell | true |
| `nexusslime.economy.admin` | Comandos de admin eco | OP |

---

## Precios de Venta (`economy/sell-prices.yml`)

```yaml
prices:
  # ── Piedra y Tierra ───────────────────────────────────────────
  COBBLESTONE:       2.0
  STONE:             3.0
  DIRT:              1.0

  # ── Madera y Plantas ──────────────────────────────────────────
  OAK_LOG:           6.0
  WHEAT:             4.0

  # ── Menas y Metales ───────────────────────────────────────────
  COAL:             10.0
  IRON_INGOT:       25.0
  GOLD_INGOT:       50.0
  DIAMOND:         200.0
  NETHERITE_INGOT: 1200.0

  # ── Drops de Mob ──────────────────────────────────────────────
  BLAZE_ROD:        20.0
  ENDER_PEARL:      25.0
  SHULKER_SHELL:   150.0
```

!!! tip
    Usa nombres de Material (mayúsculas Bukkit). Los ítems no listados en `sell-prices.yml` no pueden venderse.

---

## PlaceholderAPI

| Placeholder | Descripción |
| --- | --- |
| `%nexusslime_money%` | Saldo de dinero del jugador |
| `%nexusslime_credits%` | Saldo de créditos del jugador |

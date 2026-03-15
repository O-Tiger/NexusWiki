# Módulo Economia

O módulo Economia fornece um **sistema de moeda dupla** (dinheiro e créditos), comandos de venda, placar de riqueza e configuração de preços de venda por item.

---

## Visão Geral

| Moeda | Descrição |
| --- | --- |
| **Dinheiro** (`$`) | Moeda padrão do jogo, ganha vendendo itens, votando, etc. |
| **Créditos** | Moeda premium, normalmente obtida na webstore |

---

## Comandos

| Comando | Uso | Permissão |
| --- | --- | --- |
| `/money` | Verificar seu saldo | `nexusslime.economy.money` |
| `/money <jogador>` | Verificar saldo de outro jogador | `nexusslime.economy.money` |
| `/credits` | Verificar seus créditos | `nexusslime.economy.credits` |
| `/baltop` | Top 10 jogadores mais ricos | `nexusslime.economy.baltop` |
| `/sell hand` | Vender item na mão | `nexusslime.economy.sell` |
| `/sell all` | Vender todos os itens vendáveis | `nexusslime.economy.sell` |
| `/sell inventory` | Vender inventário completo | `nexusslime.economy.sell` |
| `/worth [item]` | Verificar valor de venda do item | `nexusslime.essentials.worth` |
| `/eco give <jogador> <quantia>` | Dar dinheiro (admin) | `nexusslime.economy.admin` |
| `/eco take <jogador> <quantia>` | Remover dinheiro (admin) | `nexusslime.economy.admin` |
| `/eco set <jogador> <quantia>` | Definir saldo (admin) | `nexusslime.economy.admin` |
| `/eco reset <jogador>` | Resetar saldo (admin) | `nexusslime.economy.admin` |

---

## Permissões

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.economy.money` | Ver saldos | true |
| `nexusslime.economy.credits` | Ver créditos | true |
| `nexusslime.economy.baltop` | Ver placar | true |
| `nexusslime.economy.sell` | Usar /sell | true |
| `nexusslime.economy.admin` | Comandos de admin eco | OP |

---

## Preços de Venda (`economy/sell-prices.yml`)

Configure os preços de venda por material usados pelo `/sell` e `/worth`.

```yaml
prices:
  # ── Pedra e Terra ─────────────────────────────────────────────
  COBBLESTONE:       2.0
  STONE:             3.0
  DIRT:              1.0

  # ── Madeira e Plantas ─────────────────────────────────────────
  OAK_LOG:           6.0
  WHEAT:             4.0

  # ── Minérios e Metais ─────────────────────────────────────────
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
    Use nomes de Material (maiúsculas Bukkit). Itens não listados em `sell-prices.yml` não podem ser vendidos.

---

## PlaceholderAPI

| Placeholder | Descrição |
| --- | --- |
| `%nexusslime_money%` | Saldo de dinheiro do jogador |
| `%nexusslime_credits%` | Saldo de créditos do jogador |

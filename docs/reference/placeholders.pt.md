# Referência PlaceholderAPI

O NexusSlime registra sua própria expansão PlaceholderAPI sob o identificador `nexusslime`. Todos os placeholders seguem o padrão `%nexusslime_<nome>%`.

**Requer:** [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) (dependência suave — instale separadamente)

---

## Economia

| Placeholder | Descrição | Exemplo |
| --- | --- | --- |
| `%nexusslime_money%` | Saldo atual de dinheiro do jogador | `12500.00` |
| `%nexusslime_credits%` | Saldo de créditos do jogador | `350` |

---

## Essenciais

| Placeholder | Descrição | Exemplo |
| --- | --- | --- |
| `%nexusslime_playtime%` | Tempo total de jogo (formatado) | `3d 12h 45m` |
| `%nexusslime_playtime_minutes%` | Tempo total de jogo em minutos | `5085` |
| `%nexusslime_homes%` | Número de homes definidos | `3` |
| `%nexusslime_afk%` | `true` se o jogador estiver AFK | `false` |
| `%nexusslime_afk_status%` | Status AFK legível por humanos | `AFK` / `Online` |

---

## Clãs

| Placeholder | Descrição | Exemplo |
| --- | --- | --- |
| `%nexusslime_clan_name%` | Nome do clã do jogador | `Shadowborn` |
| `%nexusslime_clan_tag%` | Tag do clã | `SHD` |
| `%nexusslime_clan_role%` | Cargo do jogador no clã | `Owner` / `Officer` / `Member` |
| `%nexusslime_clan_level%` | Nível atual do clã | `5` |
| `%nexusslime_clan_members%` | Contagem de membros online | `8` |
| `%nexusslime_clan_bank%` | Saldo do banco do clã | `75000.00` |

Retorna string vazia se o jogador não estiver em um clã.

---

## Crystal Defense

| Placeholder | Descrição | Exemplo |
| --- | --- | --- |
| `%nexusslime_crystal_wave%` | Número da onda atual | `7` |
| `%nexusslime_crystal_health%` | HP restante do cristal | `680.0` |
| `%nexusslime_crystal_points%` | Pontos de abate do jogador no jogo atual | `145` |
| `%nexusslime_crystal_arena%` | Nome da arena em que o jogador está | `arena1` |

Retorna string vazia se o jogador não estiver em um jogo de Crystal Defense.

---

## Segurança

| Placeholder | Descrição | Exemplo |
| --- | --- | --- |
| `%nexusslime_authenticated%` | `true` se o jogador estiver logado | `true` |
| `%nexusslime_auth_status%` | Status de autenticação legível | `Authenticated` / `Pending` |

---

## Votifier

| Placeholder | Descrição | Exemplo |
| --- | --- | --- |
| `%nexusslime_votes_total%` | Total de votos acumulados | `127` |
| `%nexusslime_vote_streak%` | Tamanho da sequência de votos atual | `12` |

---

## Estatísticas do Jogador

| Placeholder | Descrição | Exemplo |
| --- | --- | --- |
| `%nexusslime_player_blocks_broken%` | Total de blocos quebrados | `48320` |
| `%nexusslime_player_machines_placed%` | Total de máquinas colocadas | `214` |
| `%nexusslime_player_items_crafted%` | Total de itens criados | `5630` |
| `%nexusslime_player_energy_generated%` | Total de energia gerada (RF) | `1200000` |
| `%nexusslime_player_items_smelted%` | Total de itens fundidos | `890` |
| `%nexusslime_player_research_unlocked%` | Entradas de pesquisa desbloqueadas | `34` |
| `%nexusslime_player_level%` | Nível NexusSlime do jogador | `15` |
| `%nexusslime_researched_<id>%` | `true` se uma pesquisa específica estiver desbloqueada | `true` |

---

## Mochilas

| Placeholder | Descrição | Exemplo |
| --- | --- | --- |
| `%nexusslime_backpacks_owned%` | Número de mochilas que o jogador possui | `2` |

---

## Máquinas

| Placeholder | Descrição | Exemplo |
| --- | --- | --- |
| `%nexusslime_machines_count%` | Total de máquinas colocadas pelo jogador | `42` |

---

## LuckPerms

| Placeholder | Descrição | Exemplo |
| --- | --- | --- |
| `%nexusslime_lp_prefix%` | Prefixo LuckPerms do jogador | `&6[VIP]` |
| `%nexusslime_lp_suffix%` | Sufixo LuckPerms do jogador | `&7✦` |

Requerem que o LuckPerms esteja instalado.

---

## Guia

| Placeholder | Descrição |
| --- | --- |
| `%nexusslime_guide_<id>%` | Entrada dinâmica do guia para ID de item/máquina |

Esses são dinâmicos — substitua `<id>` por qualquer ID de item ou máquina registrado.

---

## Core / Diversos

| Placeholder | Descrição | Exemplo |
| --- | --- | --- |
| `%nexusslime_version%` | String da versão do plugin | `2.0.0-BETA` |
| `%nexusslime_player%` | Nome de usuário do jogador | `Steve` |
| `%nexusslime_uuid%` | UUID do jogador | `069a79f4-...` |

---

## Uso em Scoreboards / TAB

```yaml
# Exemplo com o plugin TAB
header: "&bNexusSlime &7%nexusslime_version%"
tablist-name: "%nexusslime_lp_prefix%%player_name%"
scoreboard:
  title: "&b&lSuas Estatísticas"
  lines:
    - "&7Dinheiro: &a$%nexusslime_money%"
    - "&7Créditos: &b%nexusslime_credits%"
    - "&7Votos: &e%nexusslime_votes_total% &7(sequência: %nexusslime_vote_streak%)"
    - "&7Clã: &f%nexusslime_clan_name%"
    - "&7Tempo de Jogo: &f%nexusslime_playtime%"
```

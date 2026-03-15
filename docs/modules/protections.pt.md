# Módulo Protections

O módulo Protections fornece **reivindicação de regiões por jogadores**, flags de proteção configuráveis e um **sistema de duelo 1v1**.

---

## Reivindicação de Regiões

Os jogadores selecionam dois cantos de uma região cúbica com a varinha de seleção e a reivindicam como sua área protegida. Não-membros não podem construir, quebrar ou interagir dentro da região por padrão.

### Como Reivindicar uma Região

1. Segure um **Machado Dourado** (varinha padrão)
2. Clique com o botão esquerdo em um canto da sua região → clique com o botão direito no canto oposto
3. Execute `/region claim <nome>` para reivindicar a seleção

### Comandos

| Comando | Uso | Permissão |
| --- | --- | --- |
| `/region claim <nome>` | Reivindicar área selecionada | `nexusslime.region.use` |
| `/region delete <nome>` | Excluir uma região | `nexusslime.region.use` |
| `/region list` | Listar suas regiões | `nexusslime.region.use` |
| `/region info [nome]` | Ver detalhes da região | `nexusslime.region.use` |
| `/region addmember <região> <jogador>` | Adicionar um membro | `nexusslime.region.use` |
| `/region removemember <região> <jogador>` | Remover um membro | `nexusslime.region.use` |
| `/region setflag <região> <flag> <valor>` | Definir uma flag | `nexusslime.region.use` |
| `/region flags <região>` | Ver todas as flags | `nexusslime.region.use` |
| `/protect <nome>` | Proteger rapidamente o chunk atual | `nexusslime.region.use` |
| `/region admin list [jogador]` | Admin: listar todas as regiões | `nexusslime.protect.admin` |
| `/region admin delete <nome>` | Admin: forçar exclusão de região | `nexusslime.protect.admin` |
| `/region admin setowner <região> <jogador>` | Admin: alterar proprietário | `nexusslime.protect.admin` |

---

## Flags de Região

As flags controlam o que é e não é permitido dentro de uma região.

| Flag | Valores | Padrão | Descrição |
| --- | --- | --- | --- |
| `pvp` | `true` / `false` | `false` | Permitir PvP dentro da região |
| `build` | `true` / `false` | `false` | Permitir que não-membros construam |
| `interact` | `true` / `false` | `false` | Permitir que não-membros interajam (baús, botões…) |
| `mob-spawning` | `true` / `false` | `true` | Permitir que mobs apareçam |
| `explosions` | `true` / `false` | `false` | Permitir explosões de TNT / creeper |
| `fire` | `true` / `false` | `false` | Permitir propagação de fogo |
| `greeting` | `<texto>` | — | Mensagem exibida ao entrar na região |
| `farewell` | `<texto>` | — | Mensagem exibida ao sair da região |

```bash
# Exemplo: habilitar PvP em uma região de arena
/region setflag my-arena pvp true
/region setflag my-arena greeting "&cYou entered a PvP zone!"
```

---

## Configuração (`protections/config.yml`)

```yaml
selection-wand: GOLDEN_AXE     # Item usado para selecionar cantos de região

max-regions-per-player: 5      # Máximo de regiões por jogador
max-region-volume: 100000      # Tamanho máximo da região em blocos

pvp-in-wilderness: true        # Permitir PvP fora de qualquer região

duel-request-timeout-seconds: 30

economy:
  enabled: false               # Cobrar jogadores para reivindicar regiões
  base-cost: 100.0             # Taxa fixa por reivindicação
  cost-per-block: 0.01         # Custo adicional × volume da região
  refund-percent: 50           # % reembolsado ao excluir uma região
```

---

## Sistema de Duelo

O sistema de duelo permite que os jogadores se desafiem para uma luta 1v1 em uma arena de duelo segura. Mortes durante duelos não derrubam itens.

### Comandos de Duelo

| Comando | Uso | Permissão |
| --- | --- | --- |
| `/duel <jogador>` | Desafiar um jogador para um duelo | `nexusslime.duel.use` |
| `/duel accept` | Aceitar um desafio de duelo | `nexusslime.duel.use` |
| `/duel deny` | Recusar um desafio de duelo | `nexusslime.duel.use` |
| `/duel spectate <jogador>` | Espectador de um duelo | `nexusslime.duel.use` |
| `/duel stats` | Ver suas estatísticas de duelo | `nexusslime.duel.use` |
| `/duel setarena` | Definir arena de duelo na sua localização | `nexusslime.protect.admin` |

### Regras de Duelo

- Solicitações de duelo expiram após `duel-request-timeout-seconds` (padrão: 30)
- Os itens são salvos e restaurados após o término do duelo
- O vencedor recebe recompensas configuráveis (definidas na ponte de economia)
- Ambos os jogadores são teleportados para a arena de duelo ao aceitar

---

## Permissões

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.region.use` | Criar e gerenciar próprias regiões | true |
| `nexusslime.protect.admin` | Gerenciamento administrativo de regiões | OP |
| `nexusslime.bypass.protection` | Ignorar todas as proteções de região | OP |
| `nexusslime.duel.use` | Desafiar e aceitar duelos | true |

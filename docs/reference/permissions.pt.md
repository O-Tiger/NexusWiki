# Referência de Permissões

Lista completa de todos os nós de permissão registrados pelo NexusSlime. Nós marcados como **OP** são padrão apenas para operadores; nós marcados como **true** são concedidos a todos os jogadores por padrão.

---

## Core & Admin

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.*` | Todas as permissões | OP |
| `nexusslime.command` | Usar o comando básico `/nexusslime` | true |
| `nexusslime.admin` | Acesso administrativo geral | OP |
| `nexusslime.admin.*` | Todas as permissões administrativas | OP |
| `nexusslime.admin.reload` | Recarregar configurações do plugin | OP |
| `nexusslime.admin.give` | Dar itens personalizados | OP |
| `nexusslime.admin.debug` | Alternar modo de depuração | OP |
| `nexusslime.admin.cleardata` | Limpar dados de jogadores | OP |
| `nexusslime.bypass.protection` | Ignorar todas as proteções de região | OP |

---

## Pesquisa

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.research` | Acessar sistema de pesquisa | true |
| `nexusslime.research.all` | Desbloquear toda pesquisa instantaneamente | OP |

---

## Mochilas

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.backpack.create` | Criar mochilas | true |
| `nexusslime.backpack.upgrade` | Atualizar mochilas | true |
| `nexusslime.backpack.unlimited` | Slots ilimitados de mochila | OP |

---

## Pontos de Viagem

| Permissão | Slots | Padrão |
| --- | --- | --- |
| `nexusslime.essentials.waypoints.1` | 1 ponto de viagem | true |
| `nexusslime.essentials.waypoints.5` | 5 pontos de viagem | — |
| `nexusslime.essentials.waypoints.25` | 25 pontos de viagem | — |
| `nexusslime.essentials.waypoints.unlimited` | Ilimitado | OP |
| `nexusslime.essentials.waypoint` | Acessar comandos de ponto de viagem | true |

---

## Homes

| Permissão | Slots | Padrão |
| --- | --- | --- |
| `nexusslime.essentials.homes.1` | 1 home | true |
| `nexusslime.essentials.homes.3` | 3 homes | — |
| `nexusslime.essentials.homes.10` | 10 homes | — |
| `nexusslime.essentials.homes.unlimited` | Ilimitado | OP |
| `nexusslime.essentials.home` | Usar /home, /sethome, /delhome | true |

---

## Comandos Essenciais

| Permissão | Comando | Padrão |
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
| `nexusslime.essentials.fly` | `/fly` (próprio) | false |
| `nexusslime.essentials.fly.others` | `/fly <jogador>` | OP |
| `nexusslime.essentials.hat` | `/hat` | false |
| `nexusslime.essentials.god` | `/god` (próprio) | OP |
| `nexusslime.essentials.god.others` | `/god <jogador>` | OP |
| `nexusslime.essentials.heal` | `/heal` (próprio) | OP |
| `nexusslime.essentials.heal.others` | `/heal <jogador>` | OP |
| `nexusslime.essentials.feed` | `/feed` (próprio) | OP |
| `nexusslime.essentials.feed.others` | `/feed <jogador>` | OP |
| `nexusslime.essentials.nick` | `/nick` (próprio) | false |
| `nexusslime.essentials.nick.others` | `/nick <jogador>` | OP |
| `nexusslime.essentials.afk` | `/afk` | true |
| `nexusslime.essentials.workbench` | `/workbench` | true |
| `nexusslime.essentials.trash` | `/trash` | true |
| `nexusslime.essentials.anvil` | `/anvil` | OP |
| `nexusslime.essentials.grindstone` | `/grindstone` | OP |
| `nexusslime.essentials.stonecutter` | `/stonecutter` | OP |
| `nexusslime.essentials.speed` | `/speed` | OP |
| `nexusslime.essentials.seen` | `/seen` | true |
| `nexusslime.essentials.clearinventory` | `/clearinventory` (próprio) | OP |
| `nexusslime.essentials.clearinventory.others` | `/clearinventory <jogador>` | OP |
| `nexusslime.essentials.getpos` | `/getpos` | true |
| `nexusslime.essentials.playtime` | `/playtime` | true |
| `nexusslime.essentials.gamemode` | `/gamemode` | OP |
| `nexusslime.essentials.enderchest` | `/enderchest` (próprio) | true |
| `nexusslime.essentials.enderchest.others` | `/enderchest <jogador>` | OP |
| `nexusslime.essentials.repair` | `/repair` | OP |
| `nexusslime.essentials.ext` | `/ext` | OP |
| `nexusslime.essentials.exp` | `/exp` | OP |
| `nexusslime.essentials.worth` | `/worth` | true |
| `nexusslime.essentials.rules` | `/rules` | true |
| `nexusslime.essentials.skull` | `/skull` | OP |
| `nexusslime.essentials.jail.admin` | Gerenciamento de prisão | OP |
| `nexusslime.essentials.backpack` | Comandos de mochila | true |

---

## Economia

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.economy.money` | Ver saldo de dinheiro | true |
| `nexusslime.economy.credits` | Ver créditos | true |
| `nexusslime.economy.baltop` | Ver placar | true |
| `nexusslime.economy.sell` | Usar /sell | true |
| `nexusslime.economy.admin` | Comandos administrativos de economia | OP |

---

## Clãs

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.clan.use` | Usar comandos de clã | true |
| `nexusslime.clan.admin` | Gerenciamento administrativo de clãs | OP |
| `nexusslime.clan.bypass-protection` | Ignorar território de clã | OP |

---

## Segurança

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.security.cleanworld` | Limpador de mundo manual | OP |
| `nexusslime.staff.vanish` | Tornar-se invisível | OP |
| `nexusslime.staff.vanish.others` | Tornar outro jogador invisível | OP |
| `nexusslime.staff.vanish.see` | Ver jogadores invisíveis | OP |
| `nexusslime.staff.invsee` | Inspecionar inventários | OP |
| `nexusslime.staff.spy` | Modo de espionagem de chat | OP |

---

## Chat

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.chat.staff` | Acessar canal de chat da equipe | OP |
| `nexusslime.chat.mute` | Silenciar jogadores | OP |
| `nexusslime.chat.mute.bypass` | Ignorar silenciamento | false |
| `nexusslime.chat.filter.bypass` | Ignorar filtro de palavras | OP |
| `nexusslime.chat.reload` | Recarregar configuração de chat | OP |
| `nexusslime.chat.color` | Usar códigos de cor no chat | OP |

---

## Proteções & Duelo

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.region.use` | Criar e gerenciar próprias regiões | true |
| `nexusslime.protect.admin` | Gerenciamento administrativo de regiões | OP |
| `nexusslime.duel.use` | Enviar e aceitar duelos | true |

---

## Crystal Defense

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.crystaldefense.use` | Entrar em arenas | true |
| `nexusslime.crystaldefense.admin` | Criar/gerenciar arenas | OP |

---

## Votifier

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.vote` | Usar `/vote` | true |
| `nexusslime.vote.top` | Usar `/votetop` | true |

---

## Custom Mobs

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.boss.admin` | Todos os comandos de boss/ovo de spawn | OP |

---

## Dreams

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.dreams.admin` | Comandos administrativos de sonhos | OP |

---

## Twitch

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.twitch.use` | Comandos básicos do Twitch | true |
| `nexusslime.twitch.staff` | Aprovar vinculações, realizar sorteios | OP |
| `nexusslime.twitch.admin` | Recarregar configuração do Twitch | OP |

---

## Silk Spawners

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.silkspawner.use` | Minerar spawners com Silk Touch | true |
| `nexusslime.silkspawner.admin` | Comandos administrativos de spawner | OP |

---

## Receitas & Kits

| Permissão | Descrição | Padrão |
| --- | --- | --- |
| `nexusslime.recipe` | Usar `/recipe` | true |
| `nexusslime.command.kit` | Usar `/kit` | true |
| `nexusslime.command.vip` | Usar `/vip` | true |
| `nexusslime.kit.*` | Acessar todos os kits VIP | OP |

---

## Nós de Nível de Permissão

Usados internamente para mapear cargos da equipe. Configure em `config.yml`:

| Permissão | Cargo |
| --- | --- |
| `nexusslime.level.user` | Jogador regular |
| `nexusslime.level.helper` | Auxiliar |
| `nexusslime.level.moderator` | Moderador |
| `nexusslime.level.admin` | Administrador |
| `nexusslime.level.owner` | Proprietário |

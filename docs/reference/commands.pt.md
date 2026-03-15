# Referência de Comandos

Lista completa de todos os comandos registrados pelo NexusSlime, organizados por módulo.

**Legenda:**

- `<arg>` — argumento obrigatório
- `[arg]` — argumento opcional
- `(OP)` — apenas para operadores por padrão
- `(true)` — disponível para todos os jogadores por padrão

---

## Core / Plugin

| Comando | Aliases | Descrição | Permissão |
| --- | --- | --- | --- |
| `/nexusslime help` | `/ns`, `/nexus`, `/slime` | Mostrar ajuda | `nexusslime.command` |
| `/nexusslime info` | | Versão e status do plugin | `nexusslime.command` |
| `/nexusslime reload` | | Recarregar todas as configurações | `nexusslime.admin.reload` |
| `/nexusslime give <player> <item>` | | Dar um item personalizado | `nexusslime.admin.give` |
| `/nexusslime guide` | | Abrir GUI do guia de itens | `nexusslime.command` |
| `/nexusslime modules` | | Listar todos os módulos carregados | `nexusslime.command` |
| `/nexusslime machine info <id>` | | Detalhes da máquina | `nexusslime.command` |
| `/nexusslime machine list` | | Listar todas as máquinas | `nexusslime.command` |
| `/nexusslime energy info <x,y,z>` | | Informações do nó de energia | `nexusslime.command` |
| `/nexusslime energy network` | | Ver rede de energia | `nexusslime.command` |
| `/research` | | Ver progresso de pesquisa | `nexusslime.research` |
| `/research list [tier]` | | Listar pesquisas por tier | `nexusslime.research` |
| `/research <item-id>` | | Verificar pesquisa específica | `nexusslime.research` |
| `/recipe <item>` | | Mostrar receita(s) de crafting | `nexusslime.recipe` |

---

## Mochilas & Pontos de Viagem

| Comando | Aliases | Descrição | Permissão |
| --- | --- | --- | --- |
| `/backpack open [id]` | | Abrir sua mochila | `nexusslime.essentials.backpack` |
| `/backpack list` | | Listar todas as mochilas | `nexusslime.essentials.backpack` |
| `/waypoint create <name>` | `/wp` | Criar um ponto de viagem | `nexusslime.essentials.waypoint` |
| `/waypoint delete <name>` | `/wp` | Excluir um ponto de viagem | `nexusslime.essentials.waypoint` |
| `/waypoint list` | `/wp` | Listar todos os pontos de viagem | `nexusslime.essentials.waypoint` |
| `/waypoint tp <name>` | `/wp` | Teleportar para ponto de viagem | `nexusslime.essentials.waypoint` |
| `/waypoint info <name>` | `/wp` | Informações do ponto de viagem | `nexusslime.essentials.waypoint` |

---

## Essenciais — Homes

| Comando | Descrição | Permissão |
| --- | --- | --- |
| `/home [name]` | Teleportar para um home | `nexusslime.essentials.home` |
| `/home list` | Listar todos os homes | `nexusslime.essentials.home` |
| `/sethome <name>` | Definir home na localização atual | `nexusslime.essentials.home` |
| `/delhome <name>` | Excluir um home | `nexusslime.essentials.home` |

---

## Essenciais — Warps

| Comando | Descrição | Permissão |
| --- | --- | --- |
| `/warp <name>` | Teleportar para um warp | `nexusslime.essentials.warp.use` |
| `/warp list` | Listar todos os warps | `nexusslime.essentials.warp.use` |
| `/setwarp <name>` | Criar um warp (OP) | `nexusslime.essentials.warp.admin` |
| `/delwarp <name>` | Excluir um warp (OP) | `nexusslime.essentials.warp.admin` |

---

## Essenciais — Teleportação

| Comando | Descrição | Permissão |
| --- | --- | --- |
| `/tpa <player>` | Enviar solicitação de teleporte | `nexusslime.essentials.tpa` |
| `/tpaccept` | Aceitar solicitação de teleporte | `nexusslime.essentials.tpa` |
| `/tpdeny` | Recusar solicitação de teleporte | `nexusslime.essentials.tpa` |
| `/tphere <player>` | Convocar um jogador (OP) | `nexusslime.essentials.tphere` |
| `/tppos <x> <y> <z>` | Teleportar para coordenadas (OP) | `nexusslime.essentials.tppos` |
| `/spawn` | Teleportar para o spawn | `nexusslime.essentials.spawn` |
| `/setspawn` | Definir spawn do servidor (OP) | `nexusslime.essentials.setspawn` |
| `/back` | Retornar à localização anterior | `nexusslime.essentials.back` |

---

## Essenciais — Utilidades

| Comando | Descrição | Permissão |
| --- | --- | --- |
| `/afk` | Alternar AFK | `nexusslime.essentials.afk` |
| `/fly` | Alternar voo (próprio) | `nexusslime.essentials.fly` |
| `/fly <player>` | Alternar voo (outro, OP) | `nexusslime.essentials.fly.others` |
| `/god` | Alternar modo deus | `nexusslime.essentials.god` |
| `/god <player>` | Alternar deus (outro, OP) | `nexusslime.essentials.god.others` |
| `/heal` | Curar a si mesmo (OP) | `nexusslime.essentials.heal` |
| `/heal <player>` | Curar outro (OP) | `nexusslime.essentials.heal.others` |
| `/feed` | Alimentar a si mesmo (OP) | `nexusslime.essentials.feed` |
| `/feed <player>` | Alimentar outro (OP) | `nexusslime.essentials.feed.others` |
| `/nick <name>` | Definir apelido | `nexusslime.essentials.nick` |
| `/nick <player> <name>` | Definir apelido (outro, OP) | `nexusslime.essentials.nick.others` |
| `/hat` | Usar item como chapéu | `nexusslime.essentials.hat` |
| `/speed <value>` | Definir velocidade de caminhada/voo (OP) | `nexusslime.essentials.speed` |
| `/workbench` | Bancada de trabalho portátil | `nexusslime.essentials.workbench` |
| `/anvil` | Bigorna portátil (OP) | `nexusslime.essentials.anvil` |
| `/grindstone` | Pedra de amolar portátil (OP) | `nexusslime.essentials.grindstone` |
| `/stonecutter` | Cortador de pedra portátil (OP) | `nexusslime.essentials.stonecutter` |
| `/trash` | Lixeira portátil | `nexusslime.essentials.trash` |
| `/near` | Listar jogadores próximos | `nexusslime.essentials.near` |
| `/seen <player>` | Informações da última vez online | `nexusslime.essentials.seen` |
| `/getpos` | Mostrar coordenadas | `nexusslime.essentials.getpos` |
| `/playtime` | Verificar tempo de jogo | `nexusslime.essentials.playtime` |
| `/gamemode <mode>` | Mudar modo de jogo (OP) | `nexusslime.essentials.gamemode` |
| `/enderchest` | Abrir baú do end | `nexusslime.essentials.enderchest` |
| `/enderchest <player>` | Abrir baú do end de outro (OP) | `nexusslime.essentials.enderchest.others` |
| `/clearinventory` | Limpar inventário próprio (OP) | `nexusslime.essentials.clearinventory` |
| `/clearinventory <player>` | Limpar inventário de outro (OP) | `nexusslime.essentials.clearinventory.others` |
| `/repair` | Reparar item na mão (OP) | `nexusslime.essentials.repair` |
| `/ext` | Apagar a si mesmo (OP) | `nexusslime.essentials.ext` |
| `/exp <amount>` | Dar XP (OP) | `nexusslime.essentials.exp` |
| `/skull [player]` | Obter cabeça de jogador (OP) | `nexusslime.essentials.skull` |
| `/rules` | Mostrar regras do servidor | `nexusslime.essentials.rules` |
| `/worth [item]` | Valor de venda do item | `nexusslime.essentials.worth` |

---

## Essenciais — Prisão

| Comando | Descrição | Permissão |
| --- | --- | --- |
| `/jail <player> [duration]` | Prender um jogador (OP) | `nexusslime.essentials.jail.admin` |
| `/unjail <player>` | Soltar um jogador (OP) | `nexusslime.essentials.jail.admin` |
| `/setjail` | Definir localização da prisão (OP) | `nexusslime.essentials.jail.admin` |

---

## Economia

| Comando | Descrição | Permissão |
| --- | --- | --- |
| `/money [player]` | Verificar saldo | `nexusslime.economy.money` |
| `/credits [player]` | Verificar créditos | `nexusslime.economy.credits` |
| `/baltop` | Top 10 mais ricos | `nexusslime.economy.baltop` |
| `/sell hand` | Vender item na mão | `nexusslime.economy.sell` |
| `/sell all` | Vender todos os itens vendáveis | `nexusslime.economy.sell` |
| `/sell inventory` | Vender inventário inteiro | `nexusslime.economy.sell` |
| `/worth [item]` | Verificar valor de venda | `nexusslime.essentials.worth` |
| `/eco give <player> <amount>` | Dar dinheiro (OP) | `nexusslime.economy.admin` |
| `/eco take <player> <amount>` | Retirar dinheiro (OP) | `nexusslime.economy.admin` |
| `/eco set <player> <amount>` | Definir saldo (OP) | `nexusslime.economy.admin` |
| `/eco reset <player>` | Redefinir saldo (OP) | `nexusslime.economy.admin` |

---

## Clãs

| Comando | Descrição | Permissão |
| --- | --- | --- |
| `/clan create <name> <tag>` | Criar um clã | `nexusslime.clan.use` |
| `/clan disband` | Dissolver clã | `nexusslime.clan.use` |
| `/clan invite <player>` | Convidar um jogador | `nexusslime.clan.use` |
| `/clan join <name>` | Entrar em um clã | `nexusslime.clan.use` |
| `/clan leave` | Sair do clã | `nexusslime.clan.use` |
| `/clan kick <player>` | Expulsar um membro | `nexusslime.clan.use` |
| `/clan promote <player>` | Promover a oficial | `nexusslime.clan.use` |
| `/clan demote <player>` | Rebaixar a membro | `nexusslime.clan.use` |
| `/clan info [name]` | Informações do clã | `nexusslime.clan.use` |
| `/clan list` | Listar todos os clãs | `nexusslime.clan.use` |
| `/clan chat` | Alternar chat de clã | `nexusslime.clan.use` |
| `/clan claim` | Reivindicar chunk atual | `nexusslime.clan.use` |
| `/clan unclaim` | Liberar chunk atual | `nexusslime.clan.use` |
| `/clan map` | Mostrar mapa de território | `nexusslime.clan.use` |
| `/clan chest` | Abrir baú do clã | `nexusslime.clan.use` |
| `/clan upgrade` | Abrir menu de melhorias | `nexusslime.clan.use` |
| `/clan top` | Placar de clãs | `nexusslime.clan.use` |
| `/clan admin disband <name>` | Forçar dissolução (OP) | `nexusslime.clan.admin` |
| `/clan admin unclaim <name>` | Forçar liberação (OP) | `nexusslime.clan.admin` |

---

## Segurança & Equipe

| Comando | Descrição | Permissão |
| --- | --- | --- |
| `/register <password> <confirm>` | Registrar conta | *(todos)* |
| `/login <password>` | Fazer login | *(todos)* |
| `/changepassword <old> <new>` | Alterar senha | *(autenticado)* |
| `/vanish` | Alternar invisibilidade (OP) | `nexusslime.staff.vanish` |
| `/vanish <player>` | Tornar outro invisível (OP) | `nexusslime.staff.vanish.others` |
| `/invsee <player>` | Inspecionar inventário (OP) | `nexusslime.staff.invsee` |
| `/spy` | Alternar espionagem de chat (OP) | `nexusslime.staff.spy` |
| `/cleanworld` | Executar limpador de mundo (OP) | `nexusslime.security.cleanworld` |

---

## Discord

| Comando | Descrição | Permissão |
| --- | --- | --- |
| `/discord` | Link de convite do Discord | *(todos)* |
| `/discord link` | Iniciar vinculação de conta | *(todos)* |
| `/discord unlink` | Desvincular conta | *(todos)* |
| `/discord info` | Mostrar conta vinculada | *(todos)* |
| `/discordrr` | Gerenciar cargos de reação (OP) | `nexusslime.admin` |

---

## Proteções & Duelo

| Comando | Descrição | Permissão |
| --- | --- | --- |
| `/region claim <name>` | Reivindicar área selecionada | `nexusslime.region.use` |
| `/region delete <name>` | Excluir região | `nexusslime.region.use` |
| `/region list` | Listar suas regiões | `nexusslime.region.use` |
| `/region info [name]` | Detalhes da região | `nexusslime.region.use` |
| `/region addmember <region> <player>` | Adicionar membro | `nexusslime.region.use` |
| `/region removemember <region> <player>` | Remover membro | `nexusslime.region.use` |
| `/region setflag <region> <flag> <val>` | Definir uma flag | `nexusslime.region.use` |
| `/region flags <region>` | Ver flags | `nexusslime.region.use` |
| `/protect <name>` | Proteção rápida de chunk | `nexusslime.region.use` |
| `/region admin list` | Admin: todas as regiões (OP) | `nexusslime.protect.admin` |
| `/region admin delete <name>` | Admin: excluir região (OP) | `nexusslime.protect.admin` |
| `/duel <player>` | Desafiar para duelo | `nexusslime.duel.use` |
| `/duel accept` | Aceitar duelo | `nexusslime.duel.use` |
| `/duel deny` | Recusar duelo | `nexusslime.duel.use` |
| `/duel spectate <player>` | Espectador de duelo | `nexusslime.duel.use` |
| `/duel stats` | Estatísticas de duelo | `nexusslime.duel.use` |
| `/duel setarena` | Definir arena de duelo (OP) | `nexusslime.protect.admin` |

---

## Crystal Defense

| Comando | Descrição | Permissão |
| --- | --- | --- |
| `/crystal join <arena>` | Entrar em uma arena | `nexusslime.crystaldefense.use` |
| `/crystal leave` | Sair da arena | `nexusslime.crystaldefense.use` |
| `/crystal list` | Listar arenas | `nexusslime.crystaldefense.use` |
| `/crystal status` | Onda e HP do cristal | `nexusslime.crystaldefense.use` |
| `/crystal create <name>` | Criar arena (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal delete <name>` | Excluir arena (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal setcrystal <arena>` | Definir localização do cristal (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal setspawn <arena>` | Definir spawn (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal start [arena]` | Forçar início (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal stop [arena]` | Parar jogo (OP) | `nexusslime.crystaldefense.admin` |
| `/crystal reload` | Recarregar configurações (OP) | `nexusslime.crystaldefense.admin` |

---

## Votifier

| Comando | Descrição | Permissão |
| --- | --- | --- |
| `/vote` | Mostrar links de votação e sequência | `nexusslime.vote` |
| `/votetop` | Placar de votos | `nexusslime.vote.top` |

---

## Custom Mobs

| Comando | Descrição | Permissão |
| --- | --- | --- |
| `/boss spawn <id>` | Invocar um boss | `nexusslime.boss.admin` |
| `/boss spawn <id> <w> <x> <y> <z>` | Invocar em coordenadas | `nexusslime.boss.admin` |
| `/boss list` | Listar todos os bosses | `nexusslime.boss.admin` |
| `/boss info <id>` | Definição do boss | `nexusslime.boss.admin` |
| `/boss kill <id>` | Matar todas as instâncias do boss | `nexusslime.boss.admin` |
| `/bossegg give <player> <id>` | Dar ovo de spawn | `nexusslime.boss.admin` |

---

## Dreams

| Comando | Descrição | Permissão |
| --- | --- | --- |
| `/dreams reload` | Recarregar configuração | `nexusslime.dreams.admin` |
| `/dreams trigger <player>` | Forçar sonho | `nexusslime.dreams.admin` |
| `/dreams trigger <player> nightmare` | Forçar pesadelo | `nexusslime.dreams.admin` |

---

## Twitch

| Comando | Descrição | Permissão |
| --- | --- | --- |
| `/twitch link <username>` | Iniciar vinculação | `nexusslime.twitch.use` |
| `/twitch unlink` | Desvincular conta | `nexusslime.twitch.use` |
| `/twitch status` | Status da vinculação | `nexusslime.twitch.use` |
| `/twitch approve <player>` | Aprovar vinculação (OP) | `nexusslime.twitch.staff` |
| `/twitch reject <player>` | Rejeitar vinculação (OP) | `nexusslime.twitch.staff` |
| `/twitch pending` | Solicitações pendentes (OP) | `nexusslime.twitch.staff` |
| `/twitch giveaway <streamer>` | Sortear vencedor (OP) | `nexusslime.twitch.staff` |
| `/twitch reload` | Recarregar configuração (OP) | `nexusslime.twitch.admin` |

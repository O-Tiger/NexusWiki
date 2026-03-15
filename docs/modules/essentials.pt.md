# Módulo Essenciais

O módulo Essenciais fornece **+40 comandos de qualidade de vida** cobrindo homes, warps, waypoints, teleporte, detecção de AFK, prisão e comandos utilitários do dia a dia.

---

## Homes

Jogadores podem definir homes com nome e se teletransportar para elas.

### Comandos

| Comando | Uso | Permissão |
| --- | --- | --- |
| `/home [nome]` | Teletransportar para uma home | `nexusslime.essentials.home` |
| `/home list` | Listar todas as homes | `nexusslime.essentials.home` |
| `/sethome <nome>` | Definir home na posição atual | `nexusslime.essentials.home` |
| `/delhome <nome>` | Deletar uma home | `nexusslime.essentials.home` |

### Permissões de Slots de Home

| Permissão | Slots |
| --- | --- |
| `nexusslime.essentials.homes.1` | 1 (padrão) |
| `nexusslime.essentials.homes.3` | 3 |
| `nexusslime.essentials.homes.10` | 10 |
| `nexusslime.essentials.homes.unlimited` | Ilimitado (OP) |

---

## Warps

Destinos de teletransporte públicos em todo o servidor gerenciados por admins.

### Comandos de Warps

| Comando | Uso | Permissão |
| --- | --- | --- |
| `/warp <nome>` | Teletransportar para um warp | `nexusslime.essentials.warp.use` |
| `/warp list` | Listar todos os warps | `nexusslime.essentials.warp.use` |
| `/setwarp <nome>` | Criar um warp (OP) | `nexusslime.essentials.warp.admin` |
| `/delwarp <nome>` | Deletar um warp (OP) | `nexusslime.essentials.warp.admin` |

---

## TPA (Pedidos de Teletransporte)

### Comandos TPA

| Comando | Uso | Permissão |
| --- | --- | --- |
| `/tpa <jogador>` | Enviar pedido de teletransporte | `nexusslime.essentials.tpa` |
| `/tpaccept` | Aceitar pedido de teletransporte | `nexusslime.essentials.tpa` |
| `/tpdeny` | Recusar pedido de teletransporte | `nexusslime.essentials.tpa` |
| `/tphere <jogador>` | Teletransportar jogador até você (OP) | `nexusslime.essentials.tphere` |
| `/tppos <x> <y> <z>` | Teletransportar para coordenadas (OP) | `nexusslime.essentials.tppos` |
| `/spawn` | Teletransportar para o spawn | `nexusslime.essentials.spawn` |
| `/setspawn` | Definir o spawn do servidor (OP) | `nexusslime.essentials.setspawn` |
| `/back` | Voltar para localização anterior | `nexusslime.essentials.back` |

### Configuração (`essentials/config.yml`)

```yaml
tpa:
  expiry-seconds: 60       # Pedido expira após este tempo

back:
  save-on-death: true      # Salvar localização de morte para /back
  save-on-any-teleport: false

spawn:
  respawn-at-spawn: false  # Forçar respawn no spawn (vs. cama)
```

---

## Sistema AFK

### Comandos AFK

| Comando | Uso | Permissão |
| --- | --- | --- |
| `/afk` | Alternar status AFK | `nexusslime.essentials.afk` |

### Configuração AFK

```yaml
afk:
  idle-seconds: 300        # AFK automático após 5 minutos inativo
  broadcast: true          # Anunciar quando um jogador ficar AFK
```

---

## Prisão

Admins podem enviar jogadores para uma localização de prisão predefinida.

### Comandos de Prisão

| Comando | Uso | Permissão |
| --- | --- | --- |
| `/jail <jogador> [duração]` | Prender um jogador (OP) | `nexusslime.essentials.jail.admin` |
| `/unjail <jogador>` | Soltar um jogador (OP) | `nexusslime.essentials.jail.admin` |
| `/setjail` | Definir localização da prisão (OP) | `nexusslime.essentials.jail.admin` |

---

## Comandos Utilitários

| Comando | Uso | Permissão |
| --- | --- | --- |
| `/fly` | Alternar modo de voo | `nexusslime.essentials.fly` |
| `/fly <jogador>` | Alternar voo para outro jogador (OP) | `nexusslime.essentials.fly.others` |
| `/god` | Alternar modo deus | `nexusslime.essentials.god` |
| `/heal` | Curar a si mesmo (OP) | `nexusslime.essentials.heal` |
| `/feed` | Alimentar a si mesmo (OP) | `nexusslime.essentials.feed` |
| `/nick <nome>` | Definir apelido | `nexusslime.essentials.nick` |
| `/workbench` | Bancada portátil | `nexusslime.essentials.workbench` |
| `/trash` | Lixeira portátil | `nexusslime.essentials.trash` |
| `/anvil` | Bigorna portátil (OP) | `nexusslime.essentials.anvil` |
| `/speed <valor>` | Definir velocidade de movimento (OP) | `nexusslime.essentials.speed` |
| `/near` | Listar jogadores próximos | `nexusslime.essentials.near` |
| `/seen <jogador>` | Última vez visto | `nexusslime.essentials.seen` |
| `/getpos` | Mostrar suas coordenadas | `nexusslime.essentials.getpos` |
| `/playtime` | Verificar tempo de jogo | `nexusslime.essentials.playtime` |
| `/gamemode <modo>` | Alterar modo de jogo (OP) | `nexusslime.essentials.gamemode` |
| `/enderchest` | Abrir seu baú de ender | `nexusslime.essentials.enderchest` |
| `/repair` | Reparar item segurado (OP) | `nexusslime.essentials.repair` |
| `/ext` | Apagar a si mesmo (OP) | `nexusslime.essentials.ext` |
| `/hat` | Usar item como chapéu | `nexusslime.essentials.hat` |
| `/rules` | Mostrar regras do servidor | `nexusslime.essentials.rules` |
| `/worth [item]` | Verificar valor de venda | `nexusslime.essentials.worth` |

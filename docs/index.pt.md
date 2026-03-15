# NexusSlime

> **Uma reimplementação abrangente e evolução do Slimefun4** — sistemas de tecnologia, magia e qualidade de vida de próxima geração para servidores Minecraft.

NexusSlime é um plugin Spigot modular construído sobre uma arquitetura Maven de +25 módulos. Ele traz itens personalizados, máquinas, redes de energia, clãs, economia, minijogos e integrações profundas em um único JAR leve.

---

## Funcionalidades Principais

| Categoria | Destaques |
| --- | --- |
| **Itens Personalizados** | +235 itens definidos em YAML |
| **Máquinas** | Crafting multibloco, redes de energia, armazenamento ME |
| **Economia** | Moeda dupla (dinheiro + créditos), /sell, /baltop |
| **Clãs** | Conquista de território, melhorias, baú de clã, chat de clã |
| **Essenciais** | +40 comandos QoL — homes, warps, TPA, AFK, prisão |
| **Segurança** | Auth BCrypt, anti-bot CAPTCHA, anti-dupe, anti-lag |
| **Discord** | Integração com bot, vinculação de conta, sincronização de cargos |
| **Crystal Defense** | Minijogo de defesa de Cristais Ender por ondas |
| **Mobs Personalizados** | Chefes definidos em YAML com tabelas de loot e formas de IA |
| **Votifier** | Servidor Votifier V1/V2 independente, sequências, placares |
| **Sonhos** | Sistema de cutscene de sono com variantes de pesadelo |
| **Proteções** | Reivindicação de regiões, flags, sistema de duelo |
| **Twitch** | Vinculação de conta, alertas ao vivo, relay de chat, sorteios |
| **PlaceholderAPI** | +30 placeholders em todos os módulos |

---

## Visão Geral dos Módulos

```text
NexusSlime
├── nexusslime-api          API pública para desenvolvedores de addons
├── nexusslime-core         Gerenciadores principais, registro PDC, idioma
├── nexusslime-items        Armazenamento de itens personalizados (+235 itens)
├── nexusslime-machines     Definições de máquinas, motor de processamento
├── nexusslime-systems      Implementação de redes de energia
├── nexusslime-integrations PlaceholderAPI, LuckPerms, SkinsRestorer
├── nexusslime-storage      Persistência SQLite / PostgreSQL
├── nexusslime-gui          Framework de GUI
├── nexusslime-utils        Utilitários auxiliares
├── nexusslime-web          Bridge da loja web, kits VIP, pagamentos
├── nexusslime-plugin       Ponto de entrada principal (Spigot)
├── nexusslime-discord      Bot JDA, webhooks, vinculação de conta
├── nexusslime-chat         Sistema de chat com 4 canais
├── nexusslime-ae           Armazenamento em rede estilo ME
├── nexusslime-energy       Geração de energia e redes de cabos
├── nexusslime-waila        Integração WAILA/HUD
├── nexusslime-security     Auth, anti-bot, anti-lag, anti-dupe
├── nexusslime-clans        Clãs, território, melhorias
├── nexusslime-economy      Dinheiro, créditos, preços de venda
├── nexusslime-essentials   +40 comandos QoL
├── nexusslime-crystaldefense Minijogo Crystal Defense por ondas
├── nexusslime-custommobs   Chefes definidos em YAML
├── nexusslime-dreams       Sistema de cutscene de sono
├── nexusslime-protections  Proteção de regiões, sistema de duelo
├── nexusslime-ss           Suporte a Silk Spawner
├── nexusslime-votifier     Servidor Votifier V1/V2 independente
└── nexusslime-twitch       Integração Twitch
```

---

## Navegação Rápida

| | |
| --- | --- |
| **[Primeiros Passos](getting-started.md)** | Instalação, requisitos e primeiros passos |
| **[Módulo Core](modules/core.md)** | Itens, sistema PDC, registro de itens |
| **[Todos os Módulos](modules/index.md)** | Navegue pelos 13 módulos de funcionalidades |
| **[Referência de Comandos](reference/commands.md)** | Todos os +40 comandos com uso e permissões |
| **[Referência de Permissões](reference/permissions.md)** | Lista completa de nós de permissão |
| **[PlaceholderAPI](reference/placeholders.md)** | Todos os placeholders `%nexusslime_*%` |

---

## Autor

NexusSlime é desenvolvido por **O-Tiger**

- Versão da API: `1.21`
- Dependências opcionais: `PlaceholderAPI`, `LuckPerms`, `SkinsRestorer`

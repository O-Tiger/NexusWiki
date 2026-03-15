# Changelog

Todas as mudanças notáveis no NexusSlime são documentadas aqui. O NexusSlime segue o [Versionamento Semântico](https://semver.org/).

---

## [2.0.0-BETA] — Atual

### Arquitetura

- Reescrita completa como um **projeto Maven multi-módulo com +25 módulos**
- Novo módulo `nexusslime-api` fornecendo uma API pública para desenvolvedores de addons
- Todos os sistemas de funcionalidades são agora módulos autônomos com seu próprio ciclo de vida
- Migração de persistência apenas em YAML para **SQLite / PostgreSQL** via `nexusslime-storage`

### Core

- `CustomItemRegistry` com marcação de itens baseada em PDC (`nexusslime:id`)
- Mais de 235 itens orientados a dados definidos em `items.yml`
- Sistema de tier de itens: Básico → Avançado → Infinity
- Árvore de pesquisa com desbloqueios por XP
- Suporte a múltiplos idiomas: Inglês, Português Brasileiro, Espanhol, Chinês Simplificado

### Módulos Adicionados

- **nexusslime-essentials** — Mais de 40 comandos de qualidade de vida (homes, warps, TPA, AFK, prisão, utilidades)
- **nexusslime-economy** — Sistema de dupla moeda, `/sell`, `/baltop`, preços de venda configuráveis
- **nexusslime-clans** — Reivindicação de território, árvore de melhorias, baú de clã, chat de clã
- **nexusslime-security** — Autenticação BCrypt, CAPTCHA anti-bot, detecção de VPN, anti-lag, anti-dupe
- **nexusslime-discord** — Bot JDA, vinculação de contas, sincronização de cargos, webhooks, monitoramento de GitHub Actions
- **nexusslime-crystaldefense** — Minigame cooperativo em ondas
- **nexusslime-votifier** — Servidor Votifier V1/V2 autônomo com sequências e placar
- **nexusslime-dreams** — Sistema de cutscene ao dormir (sonhos e pesadelos)
- **nexusslime-protections** — Reivindicação de regiões, flags, sistema de duelo 1v1
- **nexusslime-custommobs** — Bosses definidos em YAML com formas de IA e tabelas de loot
- **nexusslime-twitch** — Vinculação de contas, alertas ao vivo, retransmissão de chat, sorteios para espectadores
- **nexusslime-ae** — Armazenamento em rede ME (estilo Applied Energistics)
- **nexusslime-energy** — Geração de energia e redes de cabos
- **nexusslime-chat** — Chat em 4 canais (global, local, staff, comércio) com moderação
- **nexusslime-waila** — Tooltips de máquinas WAILA/HUD
- **nexusslime-ss** — Suporte a Silk Spawner
- **nexusslime-web** — Ponte de entrega de loja web, kits VIP, processamento de pagamentos, GDPR

### Integrações

- **PlaceholderAPI** — 14 provedores, mais de 30 placeholders em todos os módulos
- **LuckPerms** — Permissões e placeholders baseados em grupos
- **SkinsRestorer** — Gerenciamento de skins para servidores crackeados

### Máquinas

- `MachineYamlLoader` — máquinas definidas em `machines.yml`, sem Java necessário
- `MachineEngine` — processamento assíncrono de máquinas
- Estações de crafting multiblocos com formato de receita YAML (`infinity_recipes/`)
- Interação de máquinas baseada em GUI com `machines-gui.yml`

### Sistema de Energia

- Geradores de energia: Painéis Solares, Geradores a Carvão
- Transporte de energia baseado em cabos com perda configurável por bloco
- Capacitores para armazenamento de energia
- Redes ME para armazenamento de itens em escala

---

## [1.x] — Legado (Base Slimefun4)

> A série 1.x foi um fork/extensão direto do Slimefun4. Foi completamente substituída pela reescrita modular 2.0.

- Definições originais de itens personalizados portadas do Slimefun4
- Implementações básicas de máquinas
- Integrações iniciais de economia e chat

---

## Notas de Atualização

### Migrando de 1.x para 2.0

!!! warning
    A reescrita 2.0 **não é compatível com versões anteriores** dos arquivos de dados da 1.x.

1. Faça backup completo do seu servidor
2. Remova a pasta antiga do plugin `NexusSlime`
3. Instale o JAR 2.0 e comece do zero — as configurações são geradas automaticamente
4. Migre manualmente os dados dos jogadores se necessário usando o utilitário `NexusItemMigrator`
5. Reaaplique seu `items.yml` personalizado e as definições de receitas

---

## Próximos / Planejados

- Documentação pública da API de addons e addon de exemplo
- Painel de administração no jogo via GUI
- Ajustes dinâmicos de geração de minérios via configuração `world-generation`
- Tiers de pesquisa adicionais além de Infinity
- Suporte a cluster MySQL para grandes redes multi-servidor

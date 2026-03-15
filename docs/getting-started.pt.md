# Primeiros Passos

Esta página cobre tudo o que você precisa para instalar e configurar o NexusSlime no seu servidor.

---

## Requisitos

| Requisito | Versão |
| --- | --- |
| Servidor Minecraft | Paper / Spigot 1.21+ |
| Java | 17 ou mais recente |
| Dependência opcional | PlaceholderAPI (recomendado) |
| Dependência opcional | LuckPerms (recomendado) |
| Dependência opcional | SkinsRestorer (opcional) |

!!! warning "Aviso para Servidores Cracked"
    Se o seu servidor roda em modo offline (cracked), o sistema de autenticação do **módulo Security** é obrigatório. Contas premium são detectadas automaticamente via API Mojang e ignoram a tela de login.

---

## Instalação

1. Baixe o `NexusSlime.jar` mais recente na página de [GitHub Releases](https://github.com/O-Tiger/NexusSlime/releases).
2. Coloque o JAR na pasta `plugins/` do seu servidor.
3. Inicie o servidor uma vez para gerar todos os arquivos de configuração padrão.
4. Pare o servidor, edite as configurações geradas (veja abaixo) e reinicie.

```text
plugins/
└── NexusSlime/
    ├── config.yml
    ├── items.yml
    ├── machines.yml
    ├── lang/
    │   ├── en_US.yml
    │   ├── pt_BR.yml
    │   └── ...
    ├── security/
    ├── clans/
    ├── economy/
    ├── discord/
    ├── votifier/
    └── ...
```

---

## Configuração Principal (`config.yml`)

```yaml
settings:
  language: pt_BR         # en_US | pt_BR | es_ES | zh_CN
  debug: false
  auto-save-interval: 300 # segundos

database:
  type: SQLITE            # SQLITE ou MYSQL

  mysql:                  # Usado apenas quando type: MYSQL
    host: localhost
    port: 3306
    database: nexusslime
    username: root
    password: senha
    pool-size: 10

resourcepack:
  enabled: false
  url: ""
  sha1: ""
  force: false
  send-on-join: true

energy:
  enabled: true
  max-transfer: 1000
  loss-percentage: 5
  tick-rate: 20

machines:
  enabled: true
  max-per-chunk: 50
  tick-rate: 20
```

---

## Módulos Maven

NexusSlime é um **projeto Maven multi-módulo**. Todos os módulos são empacotados no JAR final automaticamente.

| Módulo | Descrição |
| --- | --- |
| `nexusslime-api` | API pública — interfaces para desenvolvedores de addons |
| `nexusslime-core` | Gerenciadores principais, registro PDC, sistema de idioma |
| `nexusslime-items` | Armazenamento de itens personalizados orientado a dados |
| `nexusslime-machines` | Definições de máquinas e motor de processamento |
| `nexusslime-systems` | Implementação de redes de energia |
| `nexusslime-integrations` | Hooks para PlaceholderAPI, LuckPerms, SkinsRestorer |
| `nexusslime-storage` | Persistência de dados SQLite / PostgreSQL |
| `nexusslime-gui` | Framework de GUI (menus e interfaces) |
| `nexusslime-utils` | Utilitários auxiliares |
| `nexusslime-web` | Bridge da loja web, kits VIP, processamento de pagamentos |
| `nexusslime-plugin` | Ponto de entrada principal, handler de comandos |
| `nexusslime-discord` | Bot Discord JDA, webhooks, vinculação de conta |
| `nexusslime-chat` | Sistema de chat com 4 canais e moderação |
| `nexusslime-ae` | Armazenamento em rede estilo ME |
| `nexusslime-energy` | Geradores de energia e redes de cabos |
| `nexusslime-waila` | Tooltips WAILA/HUD |
| `nexusslime-security` | Auth BCrypt, anti-bot, anti-lag, anti-dupe |
| `nexusslime-clans` | Clãs, conquista de território, melhorias |
| `nexusslime-economy` | Dinheiro, créditos, /sell, /baltop |
| `nexusslime-essentials` | +40 comandos QoL |
| `nexusslime-crystaldefense` | Minijogo Crystal Defense por ondas |
| `nexusslime-custommobs` | Chefes personalizados definidos em YAML |
| `nexusslime-dreams` | Sistema de cutscene de sono |
| `nexusslime-protections` | Proteção de regiões, flags, sistema de duelo |
| `nexusslime-ss` | Suporte a Silk Spawner |
| `nexusslime-votifier` | Servidor Votifier V1/V2 independente |
| `nexusslime-twitch` | Integração Twitch (alertas ao vivo, sorteios) |

---

## API para Desenvolvedores (Jitpack)

Adicione o NexusSlime como dependência no seu addon ou plugin usando o [Jitpack](https://jitpack.io/#O-Tiger/NexusSlime).

[![](https://jitpack.io/v/O-Tiger/NexusSlime.svg)](https://jitpack.io/#O-Tiger/NexusSlime)

!!! info "Dependência somente da API"
    Dependa de `nexusslime-api`, não de `nexusslime-plugin`, para evitar puxar a implementação completa para o seu projeto. Marque como `provided` — o JAR do plugin já está no servidor em tempo de execução.

=== "Maven"

    ```xml
    <repositories>
        <repository>
            <id>jitpack.io</id>
            <url>https://jitpack.io</url>
        </repository>
    </repositories>

    <dependencies>
        <dependency>
            <groupId>com.github.O-Tiger.NexusSlime</groupId>
            <artifactId>nexusslime-api</artifactId>
            <version>TAG</version>
            <scope>provided</scope>
        </dependency>
    </dependencies>
    ```

=== "Gradle (Kotlin DSL)"

    ```kotlin
    repositories {
        maven("https://jitpack.io")
    }

    dependencies {
        compileOnly("com.github.O-Tiger.NexusSlime:nexusslime-api:TAG")
    }
    ```

=== "Gradle (Groovy)"

    ```groovy
    repositories {
        maven { url 'https://jitpack.io' }
    }

    dependencies {
        compileOnly 'com.github.O-Tiger.NexusSlime:nexusslime-api:TAG'
    }
    ```

Substitua `TAG` pela versão do release (ex: `2.0.0-BETA`) ou um hash de commit para snapshots.

### Dependência no `plugin.yml`

```yaml
# Dependência obrigatória — seu plugin não carrega sem o NexusSlime
depend: [NexusSlime]

# Dependência opcional — carrega após o NexusSlime se presente
softdepend: [NexusSlime]
```

---

## Primeiros Passos Após a Instalação

1. **Defina seu idioma** em `config.yml` → `settings.language`
2. **Configure o módulo Security** (`security/auth.yml`) se estiver rodando offline/cracked
3. **Configure o módulo Economy** (`economy/sell-prices.yml`) com os preços dos itens
4. **Configure o Discord** (`discord/config.yml`) com seu token de bot e IDs de canais
5. **Configure o Votifier** (`votifier/config.yml`) com seus links de votação e recompensas
6. Conceda a si mesmo `nexusslime.admin.*` ou use o LuckPerms para atribuir grupos de permissões

!!! tip "Comando de recarga"
    Após alterar qualquer arquivo de configuração, execute `/nexusslime reload` para aplicar as mudanças sem reiniciar o servidor.

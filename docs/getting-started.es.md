# Primeros Pasos

Esta página cubre todo lo que necesitas para instalar y configurar NexusSlime en tu servidor.

---

## Requisitos

| Requisito | Versión |
| --- | --- |
| Servidor Minecraft | Paper / Spigot 1.21+ |
| Java | 17 o más reciente |
| Dependencia opcional | PlaceholderAPI (recomendado) |
| Dependencia opcional | LuckPerms (recomendado) |
| Dependencia opcional | SkinsRestorer (opcional) |

!!! warning "Aviso para Servidores Crackeados"
    Si tu servidor funciona en modo offline (crackeado), el sistema de autenticación del **módulo Security** es obligatorio. Las cuentas premium son detectadas automáticamente mediante la API de Mojang y omiten la pantalla de inicio de sesión.

---

## Instalación

1. Descarga el `NexusSlime.jar` más reciente desde la página de [GitHub Releases](https://github.com/O-Tiger/NexusWiki/releases).
2. Coloca el JAR en la carpeta `plugins/` de tu servidor.
3. Inicia el servidor una vez para generar todos los archivos de configuración predeterminados.
4. Detén el servidor, edita las configuraciones generadas (ver abajo) y reinicia.

```text
plugins/
└── NexusSlime/
    ├── config.yml
    ├── items.yml
    ├── machines.yml
    ├── lang/
    │   ├── en_US.yml
    │   ├── es_ES.yml
    │   └── ...
    ├── security/
    ├── clans/
    ├── economy/
    ├── discord/
    ├── votifier/
    └── ...
```

---

## Configuración Principal (`config.yml`)

```yaml
settings:
  language: es_ES         # en_US | pt_BR | es_ES | zh_CN
  debug: false
  auto-save-interval: 300 # segundos

database:
  type: SQLITE            # SQLITE o MYSQL

  mysql:                  # Solo cuando type: MYSQL
    host: localhost
    port: 3306
    database: nexusslime
    username: root
    password: contraseña
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

NexusSlime es un **proyecto Maven multi-módulo**. Todos los módulos se empaquetan en el JAR final automáticamente.

| Módulo | Descripción |
| --- | --- |
| `nexusslime-api` | API pública — interfaces para desarrolladores de addons |
| `nexusslime-core` | Gestores principales, registro PDC, sistema de idioma |
| `nexusslime-items` | Almacenamiento de ítems personalizados orientado a datos |
| `nexusslime-machines` | Definiciones de máquinas y motor de procesamiento |
| `nexusslime-systems` | Implementación de redes de energía |
| `nexusslime-integrations` | Hooks para PlaceholderAPI, LuckPerms, SkinsRestorer |
| `nexusslime-storage` | Persistencia de datos SQLite / PostgreSQL |
| `nexusslime-gui` | Framework de GUI (menús e interfaces) |
| `nexusslime-utils` | Utilidades auxiliares |
| `nexusslime-web` | Bridge de la tienda web, kits VIP, procesamiento de pagos |
| `nexusslime-plugin` | Punto de entrada principal, manejador de comandos |
| `nexusslime-discord` | Bot Discord JDA, webhooks, vinculación de cuenta |
| `nexusslime-chat` | Sistema de chat con 4 canales y moderación |
| `nexusslime-ae` | Almacenamiento en red estilo ME |
| `nexusslime-energy` | Generadores de energía y redes de cables |
| `nexusslime-waila` | Tooltips WAILA/HUD |
| `nexusslime-security` | Auth BCrypt, anti-bot, anti-lag, anti-dupe |
| `nexusslime-clanes` | Clanes, conquista de territorio, mejoras |
| `nexusslime-economy` | Dinero, créditos, /sell, /baltop |
| `nexusslime-essentials` | +40 comandos QoL |
| `nexusslime-crystaldefense` | Minijuego Crystal Defense por oleadas |
| `nexusslime-custommobs` | Jefes personalizados definidos en YAML |
| `nexusslime-dreams` | Sistema de cutscene de sueño |
| `nexusslime-protections` | Protección de regiones, banderas, sistema de duelo |
| `nexusslime-ss` | Soporte Silk Spawner |
| `nexusslime-votifier` | Servidor Votifier V1/V2 independiente |
| `nexusslime-twitch` | Integración Twitch (alertas en vivo, sorteos) |

---

## API para Desarrolladores (Jitpack)

Agrega NexusSlime como dependencia en tu addon o plugin usando [Jitpack](https://jitpack.io/#O-Tiger/NexusSlime).

[![](https://jitpack.io/v/O-Tiger/NexusSlime.svg)](https://jitpack.io/#O-Tiger/NexusSlime)

!!! info "Dependencia solo de la API"
    Depende de `nexusslime-api`, no de `nexusslime-plugin`, para evitar traer la implementación completa a tu proyecto. Márcala como `provided` — el JAR del plugin ya está en el servidor en tiempo de ejecución.

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

Reemplaza `TAG` con la versión del release (ej: `2.0.0-BETA`) o un hash de commit para snapshots.

### Dependencia en `plugin.yml`

```yaml
# Dependencia obligatoria — tu plugin no carga sin NexusSlime
depend: [NexusSlime]

# Dependencia opcional — carga después de NexusSlime si está presente
softdepend: [NexusSlime]
```

---

## Primeros Pasos Después de Instalar

1. **Configura tu idioma** en `config.yml` → `settings.language`
2. **Configura el módulo Security** (`security/auth.yml`) si tu servidor es offline/crackeado
3. **Configura el módulo Economy** (`economy/sell-prices.yml`) con los precios de los ítems
4. **Configura Discord** (`discord/config.yml`) con tu token de bot e IDs de canales
5. **Configura Votifier** (`votifier/config.yml`) con tus enlaces de votación y recompensas
6. Otórgate `nexusslime.admin.*` o usa LuckPerms para asignar grupos de permisos

!!! tip "Comando de recarga"
    Después de cambiar cualquier archivo de configuración, ejecuta `/nexusslime reload` para aplicar los cambios sin reiniciar el servidor.

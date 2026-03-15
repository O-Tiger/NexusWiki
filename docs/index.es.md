# NexusSlime

> **Una reimplementación integral y evolución de Slimefun4** — sistemas de tecnología, magia y calidad de vida de próxima generación para servidores de Minecraft.

NexusSlime es un plugin de Spigot modular construido sobre una arquitectura Maven de +25 módulos. Incluye ítems personalizados, máquinas, redes de energía, clanes, economía, minijuegos e integraciones profundas en un único JAR ligero.

---

## Características Principales

| Categoría | Destacados |
| --- | --- |
| **Ítems Personalizados** | +235 ítems definidos en YAML |
| **Máquinas** | Crafteo multibloques, redes de energía, almacenamiento ME |
| **Economía** | Moneda dual (dinero + créditos), /sell, /baltop |
| **Clanes** | Conquista de territorio, mejoras, cofre de clan, chat de clan |
| **Esenciales** | +40 comandos QoL — homes, warps, TPA, AFK, cárcel |
| **Seguridad** | Auth BCrypt, anti-bot CAPTCHA, anti-dupe, anti-lag |
| **Discord** | Integración con bot, vinculación de cuenta, sincronización de roles |
| **Crystal Defense** | Minijuego de defensa de Cristales Ender por oleadas |
| **Mobs Personalizados** | Jefes definidos en YAML con tablas de botín y formas de IA |
| **Votifier** | Servidor Votifier V1/V2 independiente, rachas, clasificaciones |
| **Sueños** | Sistema de cutscene de sueño con variantes de pesadilla |
| **Protecciones** | Reclamación de regiones, banderas, sistema de duelo |
| **Twitch** | Vinculación de cuenta, alertas en vivo, relay de chat, sorteos |
| **PlaceholderAPI** | +30 placeholders en todos los módulos |

---

## Resumen de Módulos

```text
NexusSlime
├── nexusslime-api          API pública para desarrolladores de addons
├── nexusslime-core         Gestores principales, registro PDC, idioma
├── nexusslime-items        Almacenamiento de ítems personalizados (+235 ítems)
├── nexusslime-machines     Definiciones de máquinas, motor de procesamiento
├── nexusslime-systems      Implementación de redes de energía
├── nexusslime-integrations PlaceholderAPI, LuckPerms, SkinsRestorer
├── nexusslime-storage      Persistencia SQLite / PostgreSQL
├── nexusslime-gui          Framework de GUI
├── nexusslime-utils        Utilidades auxiliares
├── nexusslime-web          Bridge de la tienda web, kits VIP, pagos
├── nexusslime-plugin       Punto de entrada principal (Spigot)
├── nexusslime-discord      Bot JDA, webhooks, vinculación de cuenta
├── nexusslime-chat         Sistema de chat con 4 canales
├── nexusslime-ae           Almacenamiento en red estilo ME
├── nexusslime-energy       Generación de energía y redes de cables
├── nexusslime-waila        Integración WAILA/HUD
├── nexusslime-security     Auth, anti-bot, anti-lag, anti-dupe
├── nexusslime-clanes       Clanes, territorio, mejoras
├── nexusslime-economy      Dinero, créditos, precios de venta
├── nexusslime-essentials   +40 comandos QoL
├── nexusslime-crystaldefense Minijuego Crystal Defense por oleadas
├── nexusslime-custommobs   Jefes definidos en YAML
├── nexusslime-dreams       Sistema de cutscene de sueño
├── nexusslime-protections  Protección de regiones, sistema de duelo
├── nexusslime-ss           Soporte Silk Spawner
├── nexusslime-votifier     Servidor Votifier V1/V2 independiente
└── nexusslime-twitch       Integración Twitch
```

---

## Navegación Rápida

| | |
| --- | --- |
| **[Primeros Pasos](getting-started.md)** | Instalación, requisitos y primeros pasos |
| **[Módulo Core](modules/core.md)** | Ítems, sistema PDC, registro de ítems |
| **[Todos los Módulos](modules/index.md)** | Explora los 13 módulos de funcionalidades |
| **[Referencia de Comandos](reference/commands.md)** | Todos los +40 comandos con uso y permisos |
| **[Referencia de Permisos](reference/permissions.md)** | Lista completa de nodos de permisos |
| **[PlaceholderAPI](reference/placeholders.md)** | Todos los placeholders `%nexusslime_*%` |

---

## Autor

NexusSlime es desarrollado por **O-Tiger**

- Versión de API: `1.21`
- Dependencias opcionales: `PlaceholderAPI`, `LuckPerms`, `SkinsRestorer`

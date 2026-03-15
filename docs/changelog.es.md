# Changelog

Todos los cambios notables en NexusSlime se documentan aquí. NexusSlime sigue el [Versionado Semántico](https://semver.org/).

---

## [2.0.0-BETA] — Actual

### Arquitectura

- Reescritura completa como un **proyecto Maven multi-módulo con +25 módulos**
- Nuevo módulo `nexusslime-api` que proporciona una API pública para desarrolladores de addons
- Todos los sistemas de funcionalidades son ahora módulos independientes con su propio ciclo de vida
- Migración de persistencia solo en YAML a **SQLite / PostgreSQL** mediante `nexusslime-storage`

### Core

- `CustomItemRegistry` con etiquetado de ítems basado en PDC (`nexusslime:id`)
- Más de 235 ítems orientados a datos definidos en `items.yml`
- Sistema de tier de ítems: Básico → Avanzado → Infinity
- Árbol de investigación con desbloqueos por XP
- Soporte multiidioma: Inglés, Portugués Brasileño, Español, Chino Simplificado

### Módulos Añadidos

- **nexusslime-essentials** — Más de 40 comandos de calidad de vida (homes, warps, TPA, AFK, prisión, utilidades)
- **nexusslime-economy** — Sistema de doble moneda, `/sell`, `/baltop`, precios de venta configurables
- **nexusslime-clans** — Reclamación de territorio, árbol de mejoras, cofre de clan, chat de clan
- **nexusslime-security** — Autenticación BCrypt, CAPTCHA anti-bot, detección de VPN, anti-lag, anti-dupe
- **nexusslime-discord** — Bot JDA, vinculación de cuentas, sincronización de roles, webhooks, monitoreo de GitHub Actions
- **nexusslime-crystaldefense** — Minijuego cooperativo por oleadas
- **nexusslime-votifier** — Servidor Votifier V1/V2 independiente con rachas y tabla de clasificación
- **nexusslime-dreams** — Sistema de cutscene al dormir (sueños y pesadillas)
- **nexusslime-protections** — Reclamación de regiones, flags, sistema de duelos 1v1
- **nexusslime-custommobs** — Bosses definidos en YAML con formas de IA y tablas de loot
- **nexusslime-twitch** — Vinculación de cuentas, alertas en directo, retransmisión de chat, sorteos para espectadores
- **nexusslime-ae** — Almacenamiento en red ME (estilo Applied Energistics)
- **nexusslime-energy** — Generación de energía y redes de cables
- **nexusslime-chat** — Chat en 4 canales (global, local, staff, comercio) con moderación
- **nexusslime-waila** — Tooltips de máquinas WAILA/HUD
- **nexusslime-ss** — Soporte para Silk Spawner
- **nexusslime-web** — Puente de entrega de tienda web, kits VIP, procesamiento de pagos, GDPR

### Integraciones

- **PlaceholderAPI** — 14 proveedores, más de 30 placeholders en todos los módulos
- **LuckPerms** — Permisos y placeholders basados en grupos
- **SkinsRestorer** — Gestión de skins para servidores crackeados

### Máquinas

- `MachineYamlLoader` — máquinas definidas en `machines.yml`, sin Java necesario
- `MachineEngine` — procesamiento asíncrono de máquinas
- Estaciones de crafteo multibloques con formato de receta YAML (`infinity_recipes/`)
- Interacción de máquinas basada en GUI con `machines-gui.yml`

### Sistema de Energía

- Generadores de energía: Paneles Solares, Generadores de Carbón
- Transporte de energía basado en cables con pérdida configurable por bloque
- Capacitores para almacenamiento de energía
- Redes ME para almacenamiento de ítems a gran escala

---

## [1.x] — Legado (Base Slimefun4)

> La serie 1.x fue un fork/extensión directo de Slimefun4. Ha sido completamente reemplazada por la reescritura modular 2.0.

- Definiciones originales de ítems personalizados portadas desde Slimefun4
- Implementaciones básicas de máquinas
- Integraciones tempranas de economía y chat

---

## Notas de Actualización

### Migración de 1.x a 2.0

!!! warning
    La reescritura 2.0 **no es compatible con versiones anteriores** de los archivos de datos de 1.x.

1. Haz una copia de seguridad completa de tu servidor
2. Elimina la carpeta antigua del plugin `NexusSlime`
3. Instala el JAR 2.0 y comienza desde cero — las configuraciones se generan automáticamente
4. Migra manualmente los datos de jugadores si es necesario usando la utilidad `NexusItemMigrator`
5. Vuelve a aplicar tu `items.yml` personalizado y las definiciones de recetas

---

## Próximos / Planificados

- Documentación pública de la API de addons y addon de ejemplo
- Panel de administración en el juego mediante GUI
- Ajustes dinámicos de generación de minerales mediante configuración `world-generation`
- Tiers de investigación adicionales más allá de Infinity
- Soporte de clúster MySQL para grandes redes multi-servidor

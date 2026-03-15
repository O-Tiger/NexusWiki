# Módulo Seguridad

El módulo Seguridad proporciona **autenticación BCrypt**, protección anti-bot con CAPTCHA, gestión de sesiones, anti-duplicación y herramientas anti-lag — diseñado para **servidores offline/crackeados**.

---

## Sub-sistemas

| Sub-sistema | Descripción |
| --- | --- |
| **Auth** | Registro/inicio de sesión con contraseñas BCrypt, sesiones persistentes |
| **Anti-Bot** | Limitación de tasa por IP, CAPTCHA en mapa, lista negra de nombres, detección de VPN |
| **Anti-Dupe** | Detecta y previene exploits comunes de duplicación de ítems |
| **Anti-Lag** | Limpiador de mundo programado, apilador de entidades |

---

## Autenticación

Los jugadores en servidores crackeados deben `/register` en el primer acceso y `/login` en los accesos siguientes. Las cuentas premium son verificadas mediante la API de Mojang y omiten la autenticación.

### Comandos

| Comando | Uso | Permiso |
| --- | --- | --- |
| `/register <contraseña> <confirmar>` | Registrar una cuenta | *(todos)* |
| `/login <contraseña>` | Iniciar sesión | *(todos)* |
| `/changepassword <antigua> <nueva>` | Cambiar contraseña | *(autenticado)* |

### Configuración Auth (`security/auth.yml`)

```yaml
storage: sqlite

session-timeout-minutes: 30      # Re-login tras 30min inactivo
persistent-session-hours: 2      # Auto-login en 2h tras última sesión

max-failed-attempts: 5           # Bloqueo tras 5 contraseñas incorrectas
lockout-minutes: 10

login-spawn:
  enabled: false
```

---

## Anti-Bot

### Configuración (`security/antibot.yml`)

```yaml
rate-limit:
  window-seconds: 10
  max-joins: 3

name-blacklist-patterns:
  - "[A-Za-z]{1,3}[0-9]{5,}"
  - "bot[0-9]+"

captcha:
  enabled: true
  timeout-seconds: 60
  session-hours: 24

premium-check:
  enabled: true

alt-detection:
  max-accounts-per-ip: 3
```

---

## Anti-Lag

### Comandos

| Comando | Uso | Permiso |
| --- | --- | --- |
| `/cleanworld` | Ejecutar limpieza manual del mundo | `nexusslime.security.cleanworld` |

### Configuración (`security/antilag.yml`)

```yaml
cleaner:
  interval-seconds: 300
  warn-seconds: 5
  item-age-ticks: 6000
  worlds:
    - world
    - world_nether

stacker:
  radius: 5.0
  max-stack: 50
```

---

## Comandos de Staff

| Comando | Uso | Permiso |
| --- | --- | --- |
| `/vanish` | Alternar invisibilidad (OP) | `nexusslime.staff.vanish` |
| `/invsee <jugador>` | Inspeccionar inventario (OP) | `nexusslime.staff.invsee` |
| `/spy` | Alternar espionaje de chat (OP) | `nexusslime.staff.spy` |

---

## Permisos

| Permiso | Descripción | Predeterminado |
| --- | --- | --- |
| `nexusslime.security.cleanworld` | Limpieza manual del mundo | OP |
| `nexusslime.staff.vanish` | Volverse invisible | OP |
| `nexusslime.staff.invsee` | Inspeccionar inventarios | OP |
| `nexusslime.staff.spy` | Modo espía de chat | OP |

---

## PlaceholderAPI

| Placeholder | Descripción |
| --- | --- |
| `%nexusslime_authenticated%` | `true` si el jugador está autenticado |
| `%nexusslime_auth_status%` | Estado de auth legible (`Autenticado`, `Pendiente`) |

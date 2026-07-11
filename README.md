# Creator Members TIDAL Family

Script de automatización en Python con Playwright para la aceptación y gestión automatizada de invitaciones de TIDAL Family.

## Características

- **Aislamiento de Ventanas**: Abre cada invitación en un contexto virtual de incógnito independiente, evitando conflictos de sesión.
- **Bypass de Pantalla de Código**: Cambia automáticamente el flujo de inicio de sesión de código/passwordless al flujo clásico de contraseña tradicional.
- **Resolución de Captchas**: Implementa un arrastre biológico simulado del ratón para resolver verificaciones humanas de DataDome.
- **Manejo de Bloqueos y Cookies**: Acepta automáticamente banners de cookies multi-frame y esquiva bloqueos temporales de red.

## Requisitos

- Python 3.8 o superior
- Google Chrome instalado en el sistema

## Instalación

1. Descarga o clona los archivos del proyecto en tu máquina.
2. Instala la librería Playwright:
   ```bash
   pip install playwright
   ```
3. Instala los binarios del navegador:
   ```bash
   playwright install chromium
   ```

## Configuración

Asegúrate de tener los siguientes archivos en la misma carpeta que el script:

1. **`invitaciones.txt`**: Contiene las URLs de invitación y los correos asignados en orden:
   ```text
   https://tidal.com/family/accept-invite/ejemplo-uuid
   correo: email_asociado@gmail.com
   ```

2. **`cuentastidal.txt`**: Contiene las credenciales de tus cuentas para el inicio de sesión automático (formato: `email contraseña` separados por espacio):
   ```text
   email_asociado@gmail.com contrasena123
   ```

## Uso

Ejecuta el script desde tu terminal:
```bash
python aceptar_invitaciones_tidal.py
```

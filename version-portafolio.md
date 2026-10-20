# Full Workspace

## Descripción breve (tarjeta)

Extension Pack para VS Code que instala en un solo paso 9 extensiones seleccionadas para el trabajo full stack: APIs, bases de datos, servidores remotos por SSH, servidor local y navegación de código.

## Descripción completa

Full Workspace es un **Extension Pack** de Visual Studio Code publicado por `alvarosiles`. Al instalarlo, VS Code descarga e instala estas extensiones del Marketplace:

| Extensión | Para qué sirve |
|---|---|
| Bookmarks | Marcar líneas y volver a ellas |
| Path Intellisense | Autocompletar rutas de archivos en los imports |
| Postman | Probar APIs sin salir del editor |
| Spanish Language Pack | Interfaz de VS Code en español |
| Remote - SSH | Trabajar en servidores remotos por SSH |
| Remote - SSH: Editing Configuration Files | Editar la configuración SSH con autocompletado |
| PowerShell | Soporte del lenguaje PowerShell |
| Database Client | Administrar bases de datos desde VS Code |
| Live Server | Servidor local con recarga automática |

Durante la verificación, la instalación del `.vsix` 0.0.3 en un perfil limpio instaló las 9 extensiones más 2 dependencias que ellas declaran: Remote Explorer y Database Client JDBC.

## Problema que resuelve

Preparar un VS Code nuevo, o el de otro miembro del equipo, para trabajar con APIs, bases de datos y servidores remotos obliga a buscar e instalar cada extensión por separado.

## Objetivo

Reproducir el entorno de trabajo completo con una sola instalación y distribuirlo por el Marketplace.

## Público objetivo

Desarrolladores full stack de habla hispana que trabajan con APIs REST, bases de datos SQL y despliegues en servidores por SSH.

## Mi participación técnica

Confirmado por el historial de git: autor de los 5 commits del repositorio (2026-07-12 → 2026-10-20). Esto incluye la selección de las extensiones, el manifiesto, el README bilingüe y el script de publicación.

## Funcionalidades destacadas

- Instalación con un clic de 9 extensiones curadas.
- README bilingüe (inglés y español) con la tabla de extensiones y su propósito.
- Plantilla reutilizable: basta con cambiar la lista de IDs en `extensionPack`.
- Script `scripts/publish.ps1` que automatiza la publicación:
  - sube la versión (`patch` / `minor` / `major` / `none`);
  - hace el commit con la versión en el mensaje;
  - genera el paquete con `vsce package`;
  - hace push y publica de forma opcional (`-Push`, `-Publish`).

## Tecnologías

| Categoría | Tecnologías |
|---|---|
| Plataforma | VS Code Extension Pack (`extensionPack`), VS Code ^1.93 |
| Automatización | PowerShell, npm (`npm version`), `@vscode/vsce` (vía `npx`) |
| Distribución | Visual Studio Code Marketplace |

## Arquitectura

El proyecto es declarativo y no tiene código de ejecución. `package.json` define los metadatos de la galería (ícono, banner, categoría *Extension Packs*) y el arreglo `extensionPack`. VS Code resuelve esa lista en el momento de la instalación. El script de publicación encadena los pasos con `$ErrorActionPreference = 'Stop'` y revisa `$LASTEXITCODE` en cada comando, así que un fallo detiene el proceso.

## Integraciones

Visual Studio Code Marketplace, y a través de las extensiones incluidas: Postman, motores de bases de datos (Database Client) y servidores SSH.

## Seguridad

- El pack no ejecuta código propio.
- Algunas extensiones incluidas manejan credenciales: cuentas de Postman, conexiones de bases de datos y llaves SSH. Las gestiona cada extensión.
- El script de publicación no guarda tokens; el acceso al Marketplace depende de `vsce login`.

## Retos técnicos

- Elegir extensiones que no se superpongan entre sí.
- Mantener el versionado y la publicación reproducibles con un solo comando.

## Mejoras futuras recomendadas

- **Actualizar el CHANGELOG**: hoy describe una versión 1.0.0 con las extensiones "Pro VSCode", que no coincide con el contenido actual (0.0.3, extensiones de terceros).
- **Sacar del repositorio los archivos ajenos al proyecto**: `z1.md`, `z2.md`, `z3.md` (análisis de fútbol), `futbol.xlsx`, `futbol_debug_extraction/` y `.vscode/settings.json`, que tiene una ruta absoluta del equipo local.
- Ordenar el historial de versiones: los mensajes de commit pasan por "version 1 (v1.0.1)" antes de volver a v0.0.2.
- Agregar una captura del pack al README del Marketplace.

## Estado

Versión `0.0.3`. El README enlaza la página del Marketplace (`alvarosiles.full-workspace`) y hay paquetes `.vsix` de las versiones 0.0.2 y 0.0.3 en el directorio de trabajo; los `.vsix` están ignorados en git.

## Capturas

| Archivo | Contenido |
|---|---|
| `presentacion/01-vista-principal.png` | VS Code justo después de instalar el pack: la lista de extensiones instaladas, con **Full Workspace** y su indicador de 9 extensiones, la pestaña de bienvenida de Postman y **Go Live** (Live Server) en la barra de estado. |
| `presentacion/02-funcionalidad-principal.png` | **Bookmarks** en uso: dos marcadores en un módulo de API y el panel lateral que los lista. |
| `presentacion/03-funcionalidad-complementaria.png` | **Path Intellisense** sugiriendo carpetas y archivos al escribir un `import`. |

Las capturas se tomaron instalando el `.vsix` real del pack en un perfil aislado de VS Code, sobre un proyecto de demostración.

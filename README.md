# 🚀 Full Workspace

[![Version](https://img.shields.io/visual-studio-marketplace/v/alvarosiles.full-workspace?color=blue)](https://marketplace.visualstudio.com/items?itemName=alvarosiles.full-workspace)
[![Installs](https://img.shields.io/visual-studio-marketplace/i/alvarosiles.full-workspace)](https://marketplace.visualstudio.com/items?itemName=alvarosiles.full-workspace)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

**🌐 Language / Idioma:** [English](#-english) · [Español](#-español)

---

## 🇬🇧 English

A curated Visual Studio Code Extension Pack to create a complete, powerful, and productive development workspace. 🛠️✨

Install this pack and get everything set up in one click — no need to search and install each extension separately.

### What's included

| Extension | Purpose |
| --- | --- |
| [Bookmarks](https://marketplace.visualstudio.com/items?itemName=alefragnani.Bookmarks) | Mark lines and jump back to them |
| [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense) | Autocompletes filenames in import paths |
| [Postman](https://marketplace.visualstudio.com/items?itemName=Postman.postman-for-vscode) | Build and test APIs without leaving the editor |
| [Spanish Language Pack](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-es) | Spanish UI language pack for VS Code |
| [Remote - SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh) | Connect to remote machines over SSH |
| [Remote - SSH: Editing Configuration Files](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh-edit) | Edit SSH config files with IntelliSense |
| [PowerShell](https://marketplace.visualstudio.com/items?itemName=ms-vscode.PowerShell) | Rich language support for PowerShell |
| [Database Client](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-database-client2) | Manage databases directly from VS Code |
| [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) | Launch a local dev server with live reload |

### Installation

Install from the [Visual Studio Code Marketplace](https://marketplace.visualstudio.com/vscode) — search for **Full Workspace**.

### Reusing this pack

This project is just a `package.json` with an [`extensionPack`](package.json) field — no build step required. Feel free to fork it and swap the list of extension IDs for your own:

```json
"extensionPack": [
  "publisher.extension-id"
]
```

Then package and publish with [`vsce`](https://github.com/microsoft/vscode-vsce):

```bash
npm install -g @vscode/vsce
vsce package
```

---

## 🇪🇸 Español

Un pack curado de extensiones para Visual Studio Code que crea un entorno de desarrollo completo, potente y productivo. 🛠️✨

Instala este pack y ten todo listo con un solo clic — sin necesidad de buscar e instalar cada extensión por separado.

### Qué incluye

| Extensión | Propósito |
| --- | --- |
| [Bookmarks](https://marketplace.visualstudio.com/items?itemName=alefragnani.Bookmarks) | Marca líneas y vuelve a ellas rápidamente |
| [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense) | Autocompleta nombres de archivo en las rutas de importación |
| [Postman](https://marketplace.visualstudio.com/items?itemName=Postman.postman-for-vscode) | Crea y prueba APIs sin salir del editor |
| [Spanish Language Pack](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-es) | Paquete de idioma español para la interfaz de VS Code |
| [Remote - SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh) | Conéctate a máquinas remotas vía SSH |
| [Remote - SSH: Editing Configuration Files](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh-edit) | Edita archivos de configuración SSH con autocompletado |
| [PowerShell](https://marketplace.visualstudio.com/items?itemName=ms-vscode.PowerShell) | Soporte completo para el lenguaje PowerShell |
| [Database Client](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-database-client2) | Administra bases de datos directamente desde VS Code |
| [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) | Levanta un servidor local con recarga automática |

### Instalación

Instálalo desde el [Visual Studio Code Marketplace](https://marketplace.visualstudio.com/vscode) — busca **Full Workspace**.

### Reutilizar este pack

Este proyecto es solo un `package.json` con un campo [`extensionPack`](package.json) — no requiere pasos de build. Puedes hacer un fork y cambiar la lista de IDs de extensiones por las tuyas:

```json
"extensionPack": [
  "publisher.extension-id"
]
```

Luego empaqueta y publica con [`vsce`](https://github.com/microsoft/vscode-vsce):

```bash
npm install -g @vscode/vsce
vsce package
```

---

## License / Licencia

MIT License

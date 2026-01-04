## 🧰 1. ¿Qué es Visual Studio Code y Code - OSS?

* **Visual Studio Code (VS Code)** es el editor de código multiplataforma que Microsoft publica con actualizaciones mensuales; está basado en un proyecto de código abierto, pero incluye algunos componentes propietarios y servicios (como el Marketplace de extensiones). ([Visual Studio Code][1])
* **Code - OSS** es el **proyecto de código abierto puro** que sirve como base de VS Code; para usarlo sin los binarios de Microsoft puedes compilar desde la fuente o instalar un proyecto como **VSCodium**, que ofrece binarios preparados de Code-OSS. ([GitHub][2])

---

## 🪟 2. Instalación en **Windows** (VS Code oficial)

Esta instalación usará el instalador oficial de Microsoft:

### ✅ Requisitos previos

* Windows 10 o Windows 11 (Versiones anteriores ya no son compatibles). ([Visual Studio Code][3])

### 🔧 Pasos

1. **Descargar instalador**
   Visita la página oficial de VS Code y descarga el instalador para Windows (User Installer o System Installer) según tu caso (x64 o ARM64). ([Visual Studio Code][4])

2. **Ejecutar el instalador**
   Haz doble clic en el archivo `.exe` descargado y sigue el asistente de instalación.

3. **Opciones recomendadas durante la instalación**

   * Añadir VS Code al PATH para poder abrirlo desde la línea de comandos (`code`). ([Visual Studio Code][3])
   * Incluir opciones de contexto (por ejemplo *Open with Code*).

4. **Finalizar**
   Inicia Visual Studio Code desde el menú Inicio.

📌 **Tip:** La instalación oficial soporta actualizaciones automáticas dentro de VS Code. ([Visual Studio Code][3])

---

## 🐧 3. Instalación en **Ubuntu / Debian-based Linux**

Aquí se explica cómo instalar la versión estándar de VS Code:

### 🔧 Método A: Repositorio APT (recomendado)

1. **Actualizar el sistema**

   ```bash
   sudo apt update
   sudo apt upgrade -y
   ```

2. **Instalar dependencias**

   ```bash
   sudo apt install software-properties-common apt-transport-https wget -y
   ```

3. **Agregar la clave GPG de Microsoft**

   ```bash
   wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
   ```

4. **Agregar el repositorio de VS Code**

   ```bash
   sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
   ```

5. **Instalar VS Code**

   ```bash
   sudo apt update
   sudo apt install code -y
   ```

6. **Verificar**

   ```bash
   code --version
   ```

📌 Alternativamente, puedes usar el paquete `.deb` descargado desde la página de VS Code e instalarlo con `sudo apt install ./nombre_del_paquete.deb`. ([Ubuntu Open Source][5])

---

### 🔁 Método B: Snap

Si prefieres Snap (más simple):

```bash
sudo snap install code --classic
```

Luego ejecuta `code` para iniciar. ([GitHub][6])

---

## 🆓 4. Instalación de **Code - OSS** (versión 100% abierta)

Si tu intención es usar la **versión open-source pura del proyecto**, hay dos formas:

### A) Compilar desde la fuente

Requiere Node.js y herramientas de desarrollo, y sigue los pasos del repositorio oficial en GitHub (clonar, instalar dependencias, compilar). ([GitHub][2])

### B) Usar **VSCodium** (binarios ya compilados de Code-OSS)

* Ve a [https://vscodium.com](https://vscodium.com)
* Descarga el instalador para tu sistema (Windows `.exe`, Linux `.deb`, etc.) o sigue las instrucciones específicas del sitio. ([VSCodium][7])
* Instala como cualquier otra aplicación.
* Ejecuta con el comando `codium` (o el lanzador que instales).

💡 **Nota:** VSCodium elimina la telemetría y otros componentes de Microsoft, pero también puede cambiar cómo funcionan algunas extensiones o integrar servicios externos. ([Reddit][8])

---

## 📌 Consejos post-instalación

✅ **Instalar Git** para control de versiones:

```bash
sudo apt install git -y
```

o en Windows, descarga desde [https://git-scm.com/](https://git-scm.com/).

✅ **Extensiones útiles**
Desde VS Code / VSCodium:

* Extensiones de Python, C/C++, JavaScript, etc.
* Themes y herramientas de productividad.

---

Si quieres, también puedo darte **scripts automatizados** para estos procesos o una guía paso a paso para compilar **Code-OSS desde la fuente**. ¿Quieres eso?

[1]: https://code.visualstudio.com/docs/supporting/FAQ?utm_source=chatgpt.com "Visual Studio Code FAQ"
[2]: https://github.com/microsoft/vscode/wiki/Differences-between-the-repository-and-Visual-Studio-Code?utm_source=chatgpt.com "Differences between the repository and Visual Studio Code - GitHub"
[3]: https://code.visualstudio.com/docs/setup/windows?utm_source=chatgpt.com "Visual Studio Code on Windows"
[4]: https://code.visualstudio.com/download?utm_source=chatgpt.com "Download Visual Studio Code - Mac, Linux, Windows"
[5]: https://www.linux.digibeatrix.com/es/development-environment-setup/ubuntu-vscode-install-setup-guide/?utm_source=chatgpt.com "Guía completa para instalar y usar Visual Studio Code en Ubuntu (edición 2025) - Harnessing the Power of Open Source with Ubuntu"
[6]: https://github.com/itspriyanshuks17/Install_Code_Ubuntu?utm_source=chatgpt.com "GitHub - itspriyanshuks17/Install_Code_Ubuntu: This guide provides a detailed, step-by-step process for installing Visual Studio Code (VS Code) on an Ubuntu system. The guide covers installation via the Microsoft repository as well as via Snap."
[7]: https://vscodium.com/?utm_source=chatgpt.com "VSCodium - Open Source Binaries of VSCode"
[8]: https://www.reddit.com/r/linuxquestions/comments/sqsvjj/vscode_codeoss_vscodium/?utm_source=chatgpt.com "VSCode, Code-OSS, VSCodium ? : r/linuxquestions - Reddit"

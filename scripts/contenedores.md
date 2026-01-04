## 1. Instalación de Docker Compose en **Windows**

> En Windows moderno, **Docker Compose ya viene integrado** como plugin dentro de **Docker Desktop** (Compose v2).

### 1.1 Requisitos previos

* Windows 10/11 **64 bits**
* Virtualización habilitada en BIOS
* WSL 2 (recomendado)
* Cuenta con privilegios de administrador

### 1.2 Instalar WSL 2

Abre **PowerShell como Administrador**:

```powershell
wsl --install
```

Reinicia el sistema cuando lo solicite.

Verifica:

```powershell
wsl --status
```

---

### 1.3 Instalar Docker Desktop

1. Descarga **Docker Desktop for Windows** desde el sitio oficial de Docker.
2. Ejecuta el instalador:

   * Marca **“Use WSL 2 instead of Hyper-V”**
3. Reinicia el equipo si se solicita.
4. Abre Docker Desktop y espera a que el servicio esté activo.

---

### 1.4 Verificar Docker y Docker Compose

En PowerShell o terminal WSL:

```bash
docker --version
docker compose version
```

✔️ Si ves `Docker Compose version v2.x`, la instalación es correcta.

---

## 2. Instalación de Docker Compose en **Linux Ubuntu**

> En Ubuntu reciente, Docker Compose también se instala como **plugin oficial (Compose v2)**.

### 2.1 Actualizar el sistema

```bash
sudo apt update && sudo apt upgrade -y
```

---

### 2.2 Instalar Docker Engine

```bash
sudo apt install -y ca-certificates curl gnupg lsb-release
```

Agregar clave GPG:

```bash
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | \
sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

Agregar repositorio:

```bash
echo \
"deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

Instalar Docker:

```bash
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

---

### 2.3 Habilitar Docker sin sudo (opcional pero recomendado)

```bash
sudo usermod -aG docker $USER
newgrp docker
```

---

### 2.4 Verificar instalación

```bash
docker --version
docker compose version
```

---

## 3. Archivo `docker-compose.yml` para Jupyter Data Science Notebook

Este contenedor incluye:

* Python
* NumPy, Pandas, SciPy
* Scikit-learn
* Matplotlib, Seaborn
* JupyterLab

### 3.1 Estructura recomendada

```text
jupyter-lab/
├── docker-compose.yml
└── work/
```

El directorio `work` será persistente.

---

### 3.2 Archivo `docker-compose.yml`

```yaml
version: "3.9"

services:
  jupyter:
    image: jupyter/datascience-notebook:latest
    container_name: jupyter_datascience
    ports:
      - "8888:8888"
    volumes:
      - ./work:/home/jovyan/work
    environment:
      - JUPYTER_ENABLE_LAB=yes
    restart: unless-stopped
```

---

### 3.3 Levantar el contenedor

Desde el directorio donde está el archivo:

```bash
docker compose up -d
```

---

### 3.4 Acceder a JupyterLab

1. Revisa el token:

```bash
docker logs jupyter_datascience
```

2. Abre en el navegador:

```
http://localhost:8888
```

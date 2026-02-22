# Depwise Scanner 🔍🌐

**Depwise Scanner** es una herramienta automatizada en Bash diseñada para la enumeración rápida de subdominios y la detección de tecnologías de red, específicamente orientada a identificar si un objetivo está detrás de un CDN o WAF como **Cloudflare** o **Amazon CloudFront**.

Este script integra herramientas potentes del ecosistema de ciberseguridad y automatiza su instalación y ejecución a través de un menú interactivo y fácil de usar, ideal para desplegar rápidamente en cualquier servidor o VPS.

---

## 🚀 Características

* **Instalación Automática de Dependencias:** El script verifica automáticamente si tienes instalados `Go`, `Assetfinder` y `httpx`. Si no es así, los instala por ti.
* **Enumeración Rápida:** Utiliza `Assetfinder` para descubrir subdominios de forma pasiva y eficiente.
* **Detección de Tecnologías:** Implementa `httpx` (de ProjectDiscovery) para analizar los subdominios encontrados, obteniendo el código de estado HTTP, la dirección IP real, el título de la página y las tecnologías/CDN detectadas (ej. `[Cloudflare]`, `[Amazon CloudFront]`).
* **Menú Interactivo:** Interfaz en terminal intuitiva con opciones modulares o de escaneo completo.
* **Gestión de Resultados:** Todo el output se guarda automáticamente en archivos `.txt` organizados por dominio para su posterior análisis.

---

## 🛠️ Herramientas Utilizadas

* [Assetfinder](https://github.com/tomnomnom/assetfinder) - Por @tomnomnom
* [httpx](https://github.com/projectdiscovery/httpx) - Por ProjectDiscovery
* [Go](https://golang.org/) - Lenguaje de programación necesario para compilar las herramientas.

---

## ⚙️ Instalación

Clona el repositorio en tu máquina local o servidor VPS y dale permisos de ejecución al script. El entorno está optimizado para distribuciones basadas en Debian/Ubuntu.

```bash
# 1. Clonar el repositorio
git clone [https://github.com/Depwisescript/Escaner.git](https://github.com/Depwisescript/Escaner.git)

# 2. Entrar al directorio
cd Escaner

# 3. Dar permisos de ejecución al script
chmod +x depwise_scanner.sh

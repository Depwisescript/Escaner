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
```
💻 Uso
Para iniciar la herramienta, simplemente ejecuta el script. La primera vez que lo corras, pedirá permisos de sudo si necesita instalar las dependencias (Go, Assetfinder, httpx).

```bash
./depwise_scanner.sh
```
Opciones del Menú:
Solo buscar subdominios (Assetfinder): Te pedirá un dominio principal y generará un archivo .txt con todos los subdominios encontrados.

Detectar CDN/WAF en una lista existente (httpx): Te permite ingresar el nombre de un archivo .txt que ya contenga subdominios para analizar qué servicios corren en ellos.

Escaneo Completo Automático (Recomendado): Realiza el paso 1 y el paso 2 de forma secuencial y automatizada.

Salir: Cierra la herramienta de forma segura.

⚠️ Aviso Legal
Esta herramienta ha sido creada con fines educativos y para su uso en auditorías de seguridad autorizadas, programas de Bug Bounty y administración de sistemas propios. El uso de esta herramienta contra objetivos sin consentimiento previo mutuo es ilegal. El desarrollador no asume ninguna responsabilidad por el mal uso o daño causado por este programa.

👤 Autor
Desarrollado por @Dan3651 como parte del proyecto Depwise.

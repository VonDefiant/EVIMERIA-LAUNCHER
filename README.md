# Evimeria Launcher

<p align="center">
  <img src="app/assets/images/SealCircle.png" alt="Evimeria Launcher" width="150">
</p>

<p align="center">
  <strong>Launcher personalizado para el servidor de Minecraft Evimeria</strong>
</p>

<p align="center">
  <a href="https://github.com/VonDefiant/EVIMERIA-LAUNCHER/releases">
    <img src="https://img.shields.io/github/v/release/VonDefiant/EVIMERIA-LAUNCHER?style=flat-square" alt="Versión">
  </a>
  <a href="https://github.com/VonDefiant/EVIMERIA-LAUNCHER/blob/main/LICENSE.txt">
    <img src="https://img.shields.io/badge/license-MIT-green?style=flat-square" alt="Licencia MIT">
  </a>
  <img src="https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey?style=flat-square" alt="Plataformas">
  <a href="https://github.com/VonDefiant/EVIMERIA-LAUNCHER/releases">
    <img src="https://img.shields.io/github/downloads/VonDefiant/EVIMERIA-LAUNCHER/total?style=flat-square" alt="Descargas">
  </a>
</p>

---

## Descripcion

Evimeria Launcher es un launcher de Minecraft personalizado que permite a los jugadores conectarse facilmente al servidor de Evimeria. Gestiona automaticamente la descarga de mods, actualizaciones y configuraciones necesarias para jugar.

## Caracteristicas

- **Actualizaciones automaticas** - El launcher se actualiza automaticamente cuando hay nuevas versiones disponibles.
- **Gestion de mods** - Descarga e instala automaticamente los mods requeridos para el servidor.
- **Autenticacion Microsoft** - Inicio de sesion seguro con tu cuenta de Microsoft/Minecraft.
- **Instalacion automatica de Java** - Detecta e instala la version correcta de Java si es necesario.
- **Integracion con Discord** - Muestra tu actividad en Discord mientras juegas.
- **Interfaz intuitiva** - Diseno moderno y facil de usar.
- **Multiples cuentas** - Gestiona varias cuentas de Minecraft desde el launcher.
- **Configuracion de RAM** - Ajusta la memoria asignada al juego segun tu sistema.

## Requisitos del Sistema

| Componente | Minimo | Recomendado |
|------------|--------|-------------|
| **Sistema Operativo** | Windows 10 / macOS 10.15 / Ubuntu 20.04 | Windows 11 / macOS 12+ / Ubuntu 22.04 |
| **RAM** | 4 GB | 8 GB o mas |
| **Almacenamiento** | 4 GB libres | 8 GB libres |
| **Java** | Java 17 (instalado automaticamente) | Java 17+ |
| **Conexion** | Conexion a internet estable | Banda ancha |

## Instalacion

### Descargar

Descarga la ultima version desde la [pagina de releases](https://github.com/VonDefiant/EVIMERIA-LAUNCHER/releases):

- **Windows**: `Evimeria-Launcher-setup-X.X.X.exe`
- **macOS**: `Evimeria-Launcher-X.X.X.dmg`
- **Linux**: `Evimeria-Launcher-X.X.X.AppImage`

### Pasos

1. Descarga el instalador para tu sistema operativo
2. Ejecuta el instalador y sigue las instrucciones
3. Abre Evimeria Launcher
4. Inicia sesion con tu cuenta de Microsoft
5. Haz clic en **JUGAR**

## Desarrollo

### Requisitos previos

- [Node.js](https://nodejs.org/) v20.x.x
- [Git](https://git-scm.com/)

### Configuracion del entorno

```bash
# Clonar el repositorio
git clone https://github.com/VonDefiant/EVIMERIA-LAUNCHER.git

# Entrar al directorio
cd EVIMERIA-LAUNCHER

# Instalar dependencias
npm install

# Ejecutar en modo desarrollo
npm start
```

### Compilar para distribucion

```bash
# Windows
npm run dist:win

# macOS
npm run dist:mac

# Linux
npm run dist:linux
```

## Estructura del Proyecto

```
EVIMERIA-LAUNCHER/
├── app/
│   ├── assets/
│   │   ├── css/          # Estilos
│   │   ├── fonts/        # Fuentes
│   │   ├── images/       # Imagenes y fondos
│   │   ├── js/           # Scripts principales
│   │   │   └── scripts/  # Scripts de UI
│   │   └── lang/         # Archivos de idioma
│   ├── app.ejs           # Plantilla principal
│   ├── frame.ejs         # Marco de ventana
│   ├── landing.ejs       # Pantalla principal
│   ├── login.ejs         # Pantalla de login
│   └── settings.ejs      # Pantalla de configuracion
├── index.js              # Punto de entrada de Electron
├── package.json          # Configuracion del proyecto
└── electron-builder.yml  # Configuracion de compilacion
```

## Configuracion

### Directorio de datos

Por defecto, el launcher almacena los archivos del juego en:

- **Windows**: `%APPDATA%/.evimerialauncher`
- **macOS**: `~/Library/Application Support/.evimerialauncher`
- **Linux**: `~/.evimerialauncher`

Puedes cambiar esta ubicacion desde **Configuracion > Launcher > Directorio de Datos**.

### Memoria RAM

Ajusta la RAM desde **Configuracion > Java > Memoria**:

- **RAM Minima**: Memoria inicial asignada
- **RAM Maxima**: Limite maximo de memoria

**Recomendacion**: Configura ambos valores iguales para reducir el lag.

## Solucion de Problemas

### El launcher no inicia

1. Verifica que tienes los requisitos minimos del sistema
2. Intenta ejecutar como administrador (Windows)
3. Revisa si tu antivirus esta bloqueando el launcher

### Error de Java

El launcher instala Java automaticamente. Si hay problemas:

1. Ve a **Configuracion > Java**
2. Haz clic en **Elegir Archivo** para seleccionar manualmente el ejecutable de Java
3. Asegurate de seleccionar Java 17 o superior (64 bits)

### No puedo conectar al servidor

1. Verifica tu conexion a internet
2. Revisa que el servidor este en linea (indicador en la pantalla principal)
3. Asegurate de que tu firewall no este bloqueando Minecraft

### Los mods no se descargan

1. Verifica tu conexion a internet
2. Intenta reiniciar el launcher
3. Elimina la carpeta de instancia y vuelve a lanzar el juego

## Licencia

Este proyecto esta bajo la licencia MIT. Consulta el archivo [LICENSE.txt](LICENSE.txt) para mas detalles.

---

<p align="center">
  Hecho con amor para la comunidad de Evimeria
</p>

# Guía de Instalación y Configuración del Entorno de Desarrollo

Bienvenido al equipo. Esta guía te ayudará a configurar tu entorno de desarrollo en Windows con todos los programas necesarios. Sigue las instrucciones paso a paso para instalar y configurar las herramientas.

---

## 1. Instalación de Herramientas Base

### a. Git
1. Descarga Git desde [Git for Windows](https://git-scm.com/download/win) y sigue las instrucciones del instalador.
2. Configura Git con tus credenciales en la terminal:
   ```bash
   git config --global user.name "Tu Nombre"
   git config --global user.email "tu.email@example.com"
   ```

### b. Node.js y npm

#### Debes instalar nvm para manejar la version de node
1. Ve al repositorio oficial de nvm-windows en GitHub:
👉 https://github.com/coreybutler/nvm-windows/releases

2. Descarga el instalador más reciente (nvm-setup.exe).

3. Ejecuta el archivo y sigue las instrucciones de instalación.

4. Reinicia tu terminal después de la instalación.
5. Veridica la instalacion 
    ```bash
    nvm version
    # ~1.1.12
    ```

#### Una vez instalado **NVM**

2. En la terminar Corre estos comandos:
    ```bash
    nvm install 18.17.1
    nvm use 18.17.1
    npm install -g npm@10.8.2
    ```


2. Verifica la instalación:
    ```bash
    node -v 
    # 18.17.1
    npm -v
    # 10.8.2
    ```

### c. Descargar e instalar Python 3.12.4
1. Ve a la página oficial:
🔗 [Descargar Python 3.12.4](https://www.python.org/downloads/release/python-3124/)

2. Ejecuta el instalador y marca la opción "Add Python to PATH".

3. Ejecuta los siguientes comandos:

    ```bash
    python -m ensurepip
    python -m pip install setuptools
    ```
4. Instala y luego verifica con:

    ```bash
    python --version
    # Python 3.12.4
    ```

### d. Docker y Docker Compose
1. Descarga e instala [Docker Desktop](https://www.docker.com/products/docker-desktop/) para Windows.
2. Durante la instalación, habilita WSL2 y Docker Compose.

## 2. Bases de Datos
### a. PostgreSQL 16.3
1. Descarga PostgreSQL desde [postgresql.org](https://www.postgresql.org/) e instala la versión 16.3.
2. Durante la instalación, establece una contraseña para el usuario postgres.
3. Usa DBeaver (instalado más adelante) para conectarte a la base de datos PostgreSQL local.
### b. DBeaver
1. Descarga e instala DBeaver Community desde [dbeaver.io](https://dbeaver.io/).
2. Configura una conexión a PostgreSQL con las credenciales proporcionadas.

## 3. Instalación de Herramientas de Desarrollo y Comunicación
### a. Visual Studio Code
1. Descarga Visual Studio Code desde [code.visualstudio.com](https://code.visualstudio.com/).
2. Instala las extensiones recomendadas para el proyecto, como:
>- [Angular Language Service](https://marketplace.visualstudio.com/items?itemName=Angular.ng-template)
>- [Angular Schematics](https://marketplace.visualstudio.com/items?itemName=cyrilletuzi.angular-schematics)
>- [JavaScript - TypeScript](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-typescript-next)
>- [Auto Close Tab](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)
>- [Auto Import Configuration](https://marketplace.visualstudio.com/items?itemName=steoates.autoimport)
>- [Better Coments](https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments)
>- [Flutter](https://marketplace.visualstudio.com/items?itemName=Dart-Code.flutter)
>- [Dart](https://marketplace.visualstudio.com/items?itemName=Dart-Code.dart-code)
>- [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)

### b. Visual Studio
1. Descarga Visual Studio desde [visualstudio.microsoft.com](https://visualstudio.microsoft.com/es/).
2. Durante la instalación, selecciona las cargas de trabajo relevantes, como:
>- Desarrollo de ASP.NET y aplicaciones web
>- Desarrollo de aplicaciones .NET Core
>- Desarrollo de Node.js (opcional, según el proyecto)
### c. Insomnia
1. Descarga Insomnia desde [insomnia.rest](https://insomnia.rest/) para probar y realizar llamadas a las APIs.
2. Importa las colecciones de APIs utilizadas en el proyecto cuando estén disponibles.
### d. Slack
>- Descarga Slack desde [slack.com/downloads/windows](https://slack.com/downloads/windows).
>- Únete al workspace del equipo para facilitar la comunicación y colaboración en el proyecto.

## 4. Configuración de Desarrollo Frontend y Backend
### a. Angular CLI
1. Instala Angular CLI para el desarrollo frontend ejecutando:
    ```bash
    npm install @angular/core@16.2.11 @angular/cli@16.2.11 --save
    ```
2. Verifica la instalación:
    ```bash
    ng version
    
    #       _                      _                 _____     ___
    #     /  \   _ __   __ _ _   _| | __ _ _ __     / ___| |   |_ _|
    #    / △ \ | '_ \ / _` | | | | |/ _` | '__|   | |   | |    | |
    #   / ___ \| | | | (_| | |_| | | (_| | |      | |___| |___ | |
    #  /_/   \_\_| |_|\__, |\__,_|_|\__,_|_|       \____|_____|___|
    #                  |___/
    #Angular CLI: 16.2.11
    #Node: 18.17.1
    #Package Manager: npm 10.8.2
    #OS: win32 x64

    #Angular:
    #...

    #Package                      Version
    #------------------------------------------------------
    #@angular-devkit/architect    0.1602.11
    #@angular-devkit/core         16.2.11
    #@angular-devkit/schematics   16.2.11
    #@schematics/angular          16.2.11
    ```
### b. .NET SDK
1. Descarga e instala el .NET SDK desde [dotnet.microsoft.com](https://dotnet.microsoft.com/es-es/download/dotnet) para trabajar en el backend.
2. Verifica la instalación:
    ```bash
    dotnet --version
    ```

## 5. Configuración de Flutter y FlutterFlow
### a. Flutter SDK
1. Descarga Flutter SDK desde [flutter.dev](https://docs.flutter.dev/get-started/install/windows/mobile) y sigue las instrucciones de configuración.
2. Agrega Flutter al PATH de Windows y verifica la instalación:
    ```bash
    flutter doctor
    ```
### b. FlutterFlow
1.FlutterFlow es una herramienta de desarrollo en la nube, así que no necesita instalación local. Accede a ella en [FlutterFlow](https://app.flutterflow.io/) usando las credenciales proporcionadas.

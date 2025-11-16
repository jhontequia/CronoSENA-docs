---
sidebar_position: 1
---

# Requisitos

Antes de correr **CronoSENA** de manera local, asegúrate de contar con las siguientes herramientas instaladas en tu sistema:

##  Instalación de herramientas necesarias
- **Git**: Descárgalo e instálalo desde [git-scm.com](https://git-scm.com/downloads).
- **Visual studio code**: Descárgalo e instálalo desde [code.visualstudio.com](https://code.visualstudio.com/)
- **nvm** Para el control de versiones de node.js [nvm/github.com](https://github.com/coreybutler/nvm-windows/releases)
- **node.js** Descárgalo e instálalo desde: [nodejs.org](https://nodejs.org/es/download)
- **npm** Cuando instalas Node.js, npm viene instalado automáticamente.No necesitas instalar npm aparte.
- **composer** Descárgalo e instálalo desde: [compose.org](https://getcomposer.org/download/)   
- **php** Descarga el lenguaje de programacion en [php.com](https://windows.php.net/download/)
    (En Windows es recomendable instalarlo con XAMPP, WampServer o Laragon para evitar configuraciones manuales).
    Si deseas instalarlo de manera manual aqui te dejo los pasos para hacerlo:

    Instalación Manual de PHP en Windows 
Este es el método manual más común y recomendado para Windows, ya que la compilación desde el código fuente es más compleja.

#### Descargar PHP:
  En la sección de descargas para Windows, elige la versión estable más reciente y descarga el paquete ZIP Thread Safe (TS) si planeas usarlo con un servidor web multihilo como Apache en Windows, o Non-Thread Safe (NTS) si es solo para uso en línea de comandos (CLI) o con servidores como IIS.

*   Extraer los archivos: Descomprime el archivo ZIP descargado en una ubicación de fácil acceso, por ejemplo, C:\php.

*   Configurar las variables de entorno (Path): Para poder ejecutar PHP desde cualquier terminal (Símbolo del sistema o           PowerShell), debes añadir la ruta de tu carpeta PHP a la variable de entorno del sistema Path:

  * Busca "variables de entorno" en el menú de inicio de Windows y selecciona "Editar las variables de entorno del sistema".
    En la ventana Propiedades del sistema, haz clic en "Variables de entorno".

 *   En "Variables del sistema", busca y selecciona la variable Path, y haz clic en "Editar".

 *   Añade una nueva entrada con la ruta completa de tu carpeta PHP: **(ej. C:\php)**, y haz clic en Aceptar en todas las ventanas.

 *   Verificar la instalación: Abre una nueva ventana de Símbolo del sistema o PowerShell y ejecuta el comando ``` php -v.``` Deberías ver la versión de PHP instalada. 

 

> Asegúrate de que todas las herramientas estén correctamente instaladas y configuradas antes de continuar con el despliegue del sistema.

---
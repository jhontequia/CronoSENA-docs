---
sidebar_position: 2
---

# Proceso de Instalacion

Requiere instalar PHP, Composer, Node.js y otras dependencias necesarias. Esta opción ofrece mayor control sobre el entorno y es útil si quieres desarrollar directamente sin contenedores. Requiere más pasos y tiempo.

Sigue estos pasos para desplegar **CronoSENA** en tu entorno de desarrollo local utilizando Docker y Docker Compose.

## 1. Clonar el Repositorio

Abre tu terminal y ejecuta los siguientes comandos:

```bash
git clone https://github.com/xenthrall/CronoSENA.git
cd CronoSENA
```
 
## 2. Configurar el Entorno

El proyecto utiliza un archivo `.env` para las variables de entorno. Cópialo a partir del ejemplo:

```bash
# Navega al directorio de la aplicación
cd src

# Copia el archivo de ejemplo
cp .env.example .env
```

Las variables por defecto ya están configuradas para funcionar con `docker-compose.yml`.

## 3. Instalar dependencias desde consola

Desde la raíz del proyecto [\CronoSENA\src].
Lo puedes hacer por ejemplo con  ```cd .\src\```.

 #### !!! recuerda  estar dentro de la carpeta src para poder ejecutar los siguientes comandos:

Ejecuta los siguientes comandos si es necesario:

 # Instalar las dependencias del proyecto:
 ## Dependecias de composer
```bash
composer install
```
Una vez realizado creemos el archivo de configuracion `.env`.
Pero primero asegurate de que estas dentro de la carpeta `\src` con el siguiente comando:
```bash
cd src
```

crea el archivo de configuracion `.env`. 
```bash
cp .env.example .env
```
Despues de este proceso, realizaremos la creacion de la clave criptográfica con el siguiente comando:

```bash
php artisan key:generate
```
Una vez tengas listo la clave criptografica vamos con un paso importante y es instalar las dependencias de npm:

Con el siguiente comando 
```bash
npm install
```

## 5. Ejecuta migraciones
```bash
php artisan migrate
```
Un vez tengas listo las migraciones vamos a hacer un paso escencial y es instalar las dependencias de npm

## ¡Listo para Usar!

Abre tu navegador y esrta sera el ejemplo claro de la url que vas a utilizar:

👉 [http://localhost:8080](http://localhost:8080)

---
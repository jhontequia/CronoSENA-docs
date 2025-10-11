---
sidebar_position: 2
---

# Levantar el Entorno de Desarrollo Local

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

## 3. Levantar los Contenedores

Desde la raíz del proyecto (`/CronoSENA`), construye y levanta los servicios con Docker Compose:

```bash
docker compose up -d --build
```

Puedes verificar que los contenedores estén activos con:

```bash
docker compose ps
```

## 4. Instalar Dependencias

Ejecuta los siguientes comandos para instalar las dependencias de PHP y Node.js dentro del contenedor de la aplicación:

```bash
# Instalar dependencias de Composer (PHP)
docker compose exec app composer install

# Instalar dependencias de NPM (Node.js)
docker compose exec app npm install

# Compilar los assets con Vite (para desarrollo) solo si es necesario
docker compose exec app npm run dev
# o para producción
docker compose exec app npm run build
```

## 5. Configurar la Aplicación

Finalmente, ejecuta las migraciones y genera la clave de la aplicación Laravel:

```bash
# Generar la clave de la aplicación
docker compose exec app php artisan key:generate

# Ejecutar las migraciones para crear las tablas en la base de datos
docker compose exec app php artisan migrate
```

## ¡Listo para Usar!

Abre tu navegador y accede a la siguiente URL para ver la aplicación en funcionamiento:

👉 [http://localhost:8080](http://localhost:8080)

---
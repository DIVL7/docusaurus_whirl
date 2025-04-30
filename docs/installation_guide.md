---
sidebar_position: 2
---

# Guía de Instalación - Whirl

Esta guía describe los pasos necesarios para instalar y ejecutar la plataforma de capacitación Whirl en un entorno de desarrollo local.

## 1. Prerrequisitos

Asegúrate de tener instalados los siguientes componentes en tu sistema:

-   **Node.js:** Versión 16.x o superior (incluye npm). Puedes descargarlo desde [nodejs.org](https://nodejs.org/).
-   **Git:** Para clonar el repositorio (si aplica).
-   **Docker y Docker Compose:** (Opcional, para ejecución contenerizada). Descárgalo desde [docker.com](https://www.docker.com/).
-   **Base de Datos:** Un servidor de base de datos compatible (ej. MySQL, PostgreSQL). La configuración específica se encuentra en `config/database.js`. Asegúrate de que el servidor esté en ejecución.

## 2. Obtener el Código Fuente

Si estás trabajando con un repositorio Git, clónalo:

```bash
git clone <URL_DEL_REPOSITORIO>
cd whirl # O el nombre del directorio del proyecto
```

Si tienes los archivos del proyecto directamente, navega hasta el directorio raíz del proyecto en tu terminal.

## 3. Instalar Dependencias

Una vez en el directorio raíz del proyecto, instala las dependencias de Node.js usando npm:

```bash
npm install
```

Este comando leerá el archivo `package.json` y descargará todos los paquetes necesarios en la carpeta `node_modules`.

## 4. Configuración de la Base de Datos

-   **Crear la Base de Datos:** Crea una base de datos vacía en tu servidor de base de datos (ej. MySQL, PostgreSQL) con el nombre especificado en `config/database.js` (o en las variables de entorno si se usan).
-   **Ejecutar Esquema:** Importa el esquema de la base de datos para crear las tablas necesarias. Generalmente, esto se hace ejecutando el archivo SQL proporcionado:
    ```bash
    # Ejemplo para MySQL
    mysql -u <usuario> -p <nombre_base_datos> < db/database_schema.sql

    # Ejemplo para PostgreSQL
    psql -U <usuario> -d <nombre_base_datos> -f db/database_schema.sql
    ```
    Reemplaza `<usuario>` y `<nombre_base_datos>` con tus credenciales.
-   **Datos de Prueba (Opcional):** Si existe un archivo con datos de prueba (`db/test_data.sql`), puedes ejecutarlo de manera similar para poblar la base de datos.

## 5. Configuración del Entorno

-   Revisa los archivos dentro del directorio `config/`. Podría ser necesario crear un archivo `.env` en la raíz del proyecto si la aplicación espera variables de entorno (como credenciales de base de datos, secretos de sesión, etc.). Consulta la documentación específica del proyecto o los archivos de configuración para saber qué variables son necesarias.
-   Asegúrate de que la configuración en `config/database.js` coincida con tu entorno de base de datos (host, usuario, contraseña, nombre de la base de datos).

## 6. Ejecutar la Aplicación (Modo Desarrollo)

Puedes iniciar el servidor Node.js directamente. Revisa el archivo `package.json` para ver el comando de inicio exacto (usualmente en `scripts.start` o `scripts.dev`). Un comando común es:

```bash
npm start
```

O si existe un script de desarrollo (que podría usar `nodemon` para reinicios automáticos):

```bash
npm run dev
```

Una vez iniciado, la aplicación debería estar accesible en la URL especificada en la consola (generalmente `http://localhost:3000` o similar).

## 7. Ejecutar con Docker (Alternativa)

Si prefieres usar Docker, asegúrate de que Docker y Docker Compose estén instalados y en ejecución.

-   **Construir y Ejecutar:** Desde el directorio raíz del proyecto, ejecuta:
    ```bash
    docker-compose up --build
    ```
    Este comando construirá las imágenes de Docker (si no existen) y levantará los contenedores definidos en `docker-compose.yml` (que típicamente incluirán la aplicación Node.js y la base de datos).

-   **Acceso:** La aplicación debería estar accesible en la URL y puerto definidos en la configuración de Docker (a menudo `http://localhost:PUERTO`, donde `PUERTO` podría ser 3000 u otro especificado en `docker-compose.yml`).

-   **Detener:** Para detener los contenedores, presiona `Ctrl + C` en la terminal donde ejecutaste `docker-compose up`, y luego ejecuta:
    ```bash
    docker-compose down
    ```

Con estos pasos, deberías tener la plataforma Whirl funcionando en tu entorno local.

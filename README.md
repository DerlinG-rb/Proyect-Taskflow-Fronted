# TaskFlow — Frontend

**TaskFlow** es una moderna aplicación web de interfaz de usuario diseñada para la gestión de tareas siguiendo una metodología Kanban. Esta aplicación cliente (SPA) ofrece una experiencia fluida con funcionalidades integradas de autenticación de usuarios, así como la gestión completa de proyectos y sus respectivas tareas.

## Tecnologías Utilizadas (Stack)

- **React 18.3.0 + Vite** (Librería principal UI y empaquetador ultrarrápido)
- **React Router** (Gestión robusta de rutas y navegación)
- **Axios** (Cliente HTTP para la comunicación con la API del backend)

## Instalación y Ejecución Local

Para levantar el entorno de desarrollo del frontend en tu máquina local, asegúrate de tener instalado Node.js. Luego sigue estos pasos:

1. **Instalar dependencias:**
   Descarga e instala todos los paquetes necesarios definidos en el proyecto.
   ```bash
   npm install
   ```

2. **Configurar el entorno:**
   Crea el archivo de entorno a partir del archivo de ejemplo para configurar tus variables locales.
   ```bash
   cp .env.example .env
   ```
   Abre el archivo `.env` recién creado y asegúrate de que la variable `VITE_API_URL` apunte a la ruta de tu API backend local. Por ejemplo:
   ```env
   VITE_API_URL=http://localhost:8000/api
   ```

3. **Levantar el servidor de desarrollo:**
   Inicia el servidor local proporcionado por Vite.
   ```bash
   npm run dev
   ```
   *La aplicación frontend estará disponible por defecto en `http://localhost:5173`.*

## Compilación y Despliegue a Producción

Para generar los archivos estáticos optimizados listos para un entorno de producción, ejecuta:

```bash
npm run build
```

Este comando procesa y minifica todo el código del proyecto, depositando el resultado final en la carpeta `dist/`.

**Despliegue Automático (CI/CD vía GitHub Actions):**

Este proyecto cuenta con un flujo de despliegue automatizado, por lo que **no es necesario** subir ni gestionar la carpeta `dist/` de forma manual. 

El repositorio incluye un *workflow* de GitHub Actions configurado en `.github/workflows/deploy-pages.yml`. Su funcionamiento es el siguiente:
- Cada vez que realizas un *push* o fusionas cambios en la rama `main`, la acción se dispara automáticamente.
- Ejecuta el proceso de construcción (`npm run build`) en un entorno de la nube.
- Publica los archivos estáticos resultantes directamente en **GitHub Pages**.

La aplicación en vivo se actualiza automáticamente tras cada subida y puede ser consultada en: 
`https://DerlinG-rb.github.io/taskflow-frontend/` 
*(o en el dominio personalizado que tengas configurado en la sección Settings → Pages de tu repositorio).*

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

## Compilación para Producción (Build)

Para generar los archivos estáticos optimizados para producción, ejecuta:

```bash
npm run build
```

Este comando genera una carpeta `dist/` con todo el código minificado y listo para su despliegue. 

**Despliegue Automático (CI/CD):** 
En este repositorio, el despliegue está automatizado. No es necesario subir la carpeta `dist/` manualmente. Contamos con un workflow de GitHub Actions (`.github/workflows/deploy-pages.yml`) que ejecuta automáticamente la construcción (`npm run build`) en cada _push_ a la rama `main`, publicando el resultado directamente en **GitHub Pages**.

La aplicación en vivo se puede consultar en: `https://DerlinG-rb.github.io/taskflow-frontend/` (o en el dominio personalizado que esté configurado en _Settings → Pages_ del repositorio).

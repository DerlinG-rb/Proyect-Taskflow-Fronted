# TaskFlow — Frontend

  Taskflow es una aplicación web para la gestión de tareas tipo Kanban con
  funcionalidades de autenticación, gestión de proyectos y tareas.

## Stack

- React 18.3.0 + Vite
- React Router
- axios

## Cómo correrlo localmente

```bash
npm install
cp .env.example .env 
luego edita el .env con la URL local del backend por ejemplo 
VITE_API_URL=http://localhost:8000/api
npm run dev
```

## Build de producción

```bash
npm run build
```

`npm run build` genera `dist/` con los archivos estáticos ya optimizados. En este proyecto no se sube a mano: el workflow `.github/workflows/deploy-pages.yml` corre ese mismo comando en cada push a `main` y publica el resultado en GitHub Pages, en `https://DerlinG-rb.github.io/taskflow-frontend/` (o en el dominio propio configurado en Settings → Pages).

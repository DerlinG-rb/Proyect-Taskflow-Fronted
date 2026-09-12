# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some Oxlint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the Oxlint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and Oxlint's TypeScript related rules in your project.
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

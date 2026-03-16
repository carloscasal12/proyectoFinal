# Proyecto Restaurante
App full-stack para restaurantes, platos, pedidos y clientes.
Backend API REST en Docker; frontend React consume la API.
**Tecnologías**
- Backend: Node.js + MySQL (Docker Compose).
- Frontend: React + Vite + React Router.
- UI: MUI + DataGrid (responsive).
**Funcionalidad (requisitos)**
- Lista restaurantes y detalle por restaurante (platos, pedidos y clientes).
- Consulta platos por pedido en `/order/:id/dishes`.
- `fetch` + `async/await` con `useState`/`useEffect`.
- React Router con rutas `/` y `/restaurants/:id`.
- SPA sin recargas, actualización dinámica con estado.
- Componentes de terceros para tabla (DataGrid).
**Interfaz**
- Diseño responsive móvil y escritorio.
- Estilos con framework CSS (MUI).
**Config**
- API principal: `https://restaurants.arasaac.org`.
- API local: `http://localhost:4000`.
- Frontend dev: `restaurante-frontend/.env` (`VITE_API_URL`).
- Frontend prod: `restaurante-frontend/.env.production` (`VITE_API_URLS`).
**Arranque local (Docker)**
- Backend: `docker compose up -d` en `restaurante-backend`.
- Verifica la API en `http://localhost:4000/restaurants`.
- Frontend: `npm install` y `npm run dev` en `restaurante-frontend`.
**Despliegue (GitHub Pages)**
- `npm run build` y `npm run deploy` en `restaurante-frontend`.
- Activa GitHub Pages en la rama `gh-pages`.
**Control de versiones**
- 5+ commits con mensajes descriptivos.
- Una sola rama principal.

# Proyecto Restaurante

Aplicación full-stack para gestionar restaurantes, platos, pedidos y clientes.
El backend expone una API REST y el frontend consume esa API con React.

**Tecnologías**
- Backend: Node.js + MySQL en Docker Compose.
- Frontend: React + Vite + React Router.
- UI: MUI y DataGrid.

**Qué hace**
- Lista restaurantes.
- Muestra platos, pedidos y clientes.
- Consulta platos por pedido en `/order/:id/dishes`.
- Navegación entre `/` y `/restaurants/:id` sin recargar.

**Cómo lo he hecho**
- API en contenedor Node con conexión a MySQL.
- Base de datos inicializada con scripts en `restaurante-backend/data/initData`.
- Variables de entorno en `restaurante-backend/.env` para credenciales.
- Frontend con `fetch` + `async/await` y estado con `useState`/`useEffect`.
- Separación de páginas en `restaurante-frontend/src/pages`.
- Helper de API en `restaurante-frontend/src/api.js`.

**Puertos y endpoints**
- API: `http://localhost:4000`.
- phpMyAdmin: `http://localhost:9091`.
- Endpoints principales: `/restaurants`, `/dishes`, `/customers`, `/orders`.

**Configurar entorno**
- Backend: revisa `restaurante-backend/.env`.
- Frontend dev: `restaurante-frontend/.env` con `VITE_API_URL`.
- Frontend prod: `restaurante-frontend/.env.production` con `VITE_API_URLS`.

**Cómo activar todo (local)**
1. En `restaurante-backend`: `docker compose up -d`.
2. Verifica la API en `http://localhost:4000/restaurants`.
3. En `restaurante-frontend`: `npm install`.
4. Arranca el frontend: `npm run dev`.
5. Abre la app en la URL que indique Vite (normalmente `http://localhost:5173`).

**Despliegue**
- Compila: `npm run build`.
- Publica en GitHub Pages: `npm run deploy`.
- Activa GitHub Pages en la rama `gh-pages`.

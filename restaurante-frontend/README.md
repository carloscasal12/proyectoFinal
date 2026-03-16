# Restaurante Frontend

Aplicación React + Vite que consume la API del proyecto restaurante-backend.

## Requisitos cumplidos
- Consumo de datos externos con `fetch` y `async/await` (`/restaurants`, `/dishes`, `/orders`, `/customers`, `/order/:id/dishes`).
- Uso de `useState` y `useEffect` para carga asíncrona y actualización dinámica.
- React Router con rutas `/` y `/restaurants/:id`.
- Diseño responsive con MUI (framework CSS) y DataGrid (componente de terceros).
- Interfaz dinámica sin recarga de página.

## Puesta en marcha
1. Inicia el backend (en el repo `restaurante-backend`):
   - `docker compose up -d`
   - API en `http://localhost:4000`
2. En este frontend:
   - `npm install`
   - `npm run dev`

## Configuración
- `.env` (dev): `VITE_API_URL=http://localhost:4000`.
- `.env.production` (deploy): `VITE_API_URLS=http://51.210.22.156:4000,http://localhost:4000`.
- El frontend prueba la lista en orden y usa la primera disponible.

## Despliegue (GitHub Pages)
1. `npm run build`
2. `npm run deploy`
3. Activa GitHub Pages en la rama `gh-pages`.

## Estructura principal
- `src/pages/HomePage.jsx`: listado de restaurantes.
- `src/pages/RestaurantPage.jsx`: platos, pedidos y clientes.
- `src/api.js`: helper de peticiones.

## Notas
- El backend expone la API en el puerto 4000 vía Docker.
- El servidor externo requerido es `http://51.210.22.156:4000`.
- El detalle de cada pedido carga sus platos con `/order/:id/dishes`.

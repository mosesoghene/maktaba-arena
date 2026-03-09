# 🎨 Maktaba Arena: Frontend

This directory contains the React application for Maktaba Arena, bootstrapped with [Vite](https://vitejs.dev/) for lightning-fast development.

It handles both the Player Controller view (mobile-optimized) and the Presenter Game view (large-screen optimized).

## Tech Stack
* **Core:** React 18, React Router v6
* **State Management:** Zustand (for live WebSocket game state), React Query (for caching REST API data)
* **Styling:** Tailwind CSS
* **Build Tool:** Vite

## Docker Configuration

### Development Mode
To run the frontend in development mode with hot-reloading:
```bash
docker build --target development -t maktaba-frontend-dev .
docker run -p 3000:3000 -v $(pwd):/frontend -v /frontend/node_modules maktaba-frontend-dev
```

### Production Mode
To build and run the production-optimized version using Nginx:
```bash
docker build --target production -t maktaba-frontend-prod .
docker run -p 80:80 maktaba-frontend-prod
```

### Environment Variables
* `VITE_API_URL`: The URL of the backend API (default: `http://localhost:8000`). This can be configured in `docker-compose.yml`.

### Port Mapping
* **Development:** Exposes port `3000`.
* **Production:** Exposes port `80`.

### Hot-Reloading in Docker
Hot-reloading is enabled via Vite's polling mechanism (`usePolling: true`) in `vite.config.js`. This ensures file changes on the host machine are detected within the container even on systems with limited file event propagation.
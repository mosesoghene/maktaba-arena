# 🎨 Maktaba Arena: Frontend

This directory contains the React application for Maktaba Arena, bootstrapped with [Vite](https://vitejs.dev/) for lightning-fast development.

It handles both the Player Controller view (mobile-optimized) and the Presenter Game view (large-screen optimized).

## Tech Stack
* **Core:** React 18, React Router v6
* **State Management:** Zustand (for live WebSocket game state), React Query (for caching REST API data)
* **Styling:** Tailwind CSS
* **Build Tool:** Vite

## Local Development
This frontend is designed to run via Docker. It automatically connects to the Django backend APIs and WebSocket server.

Please use the root `docker-compose.yml` to start the frontend service:
```bash
docker-compose up frontend
```

The app will be available at http://localhost:3000.

## Installing New Packages
If you need to add a new npm package (e.g., npm install react-use-websocket), you should run the command inside the running container to keep your local machine clean:
```bash
docker-compose exec frontend npm install react-use-websocket
```
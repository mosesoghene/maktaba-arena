# ⚙️ Maktaba Arena: Backend

This directory contains the Django application that powers Maktaba Arena. It serves two primary functions:
1. **REST API:** Handles authentication, content management (subjects/questions), and player statistics.
2. **WebSocket Engine:** Powered by Django Channels and Redis, this handles the low-latency, real-time game loop.

## Tech Stack
* **Framework:** Django 5.x
* **API:** Django REST Framework (DRF)
* **WebSockets:** Django Channels
* **Database Driver:** Psycopg2 (PostgreSQL)

## Local Development
This backend is designed to be run via Docker. Please refer to the root `docker-compose.yml` to spin up this service. 

If you need to run manage.py commands (like creating migrations), execute them inside the running container:
```bash
docker-compose exec backend python manage.py makemigrations
docker-compose exec backend python manage.py migrate
```

### Adding Requirements
If you install a new Python package, remember to update the requirements file:
```bash
docker-compose exec backend pip install <package-name>
docker-compose exec backend pip freeze > requirements.txt
```

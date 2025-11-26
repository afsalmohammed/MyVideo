API endpoints (examples)

POST /api/auth/login/ → body { "username": "demo", "password": "demo123" } → response { "token": "demo-token" }

GET /api/videos/ → list of videos.

GET /api/videos/{id}/ → metadata.

GET /api/videos/{id}/stream/ → video file stream for HTML5 <video>.

Architecture overview

React SPA served by Nginx.

Nginx reverse-proxies /api and /media to Django.

Django + DRF provide auth, metadata APIs, and file streaming.

PostgreSQL stores video metadata.

Docker Compose runs db, backend, frontend, nginx.

How to run

docker-compose up --build

Visit http://localhost

Login with demo / demo123 and start watching.


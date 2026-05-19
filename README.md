# Docker Hands-On L3 — ITCS 6190

## What I Learned
In this hands-on, I learned how to install Docker Desktop and use it to run 
containerized services. I built a Python Flask web app that connects to a Redis 
cache, containerized it using a Dockerfile, and used Docker Compose to orchestrate 
both services together. I also learned about container networking, port mapping, 
and how to use `docker compose up` to spin up multiple services at once.

## Steps to Run

1. Clone the repo:
```bash
git clone https://github.com/gmakkena9/docker-lab-itcs6190.git
cd docker-lab-itcs6190
```

2. Build and run the app:
```bash
docker compose up
```

3. Open http://localhost:8000 in your browser

## Project Structure
- `app.py` — Flask web app with Redis hit counter
- `Dockerfile` — Containerizes the Python app
- `compose.yaml` — Defines web and redis services
- `requirements.txt` — Python dependencies
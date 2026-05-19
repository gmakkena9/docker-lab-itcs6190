# Docker Hands-On L3 — ITCS 6190

## What I Learned
In this hands-on lab, I learned how to install and configure Docker Desktop 
on Windows. I built a Python Flask web application that uses Redis as a cache 
to count page visits. I containerized the Flask app using a Dockerfile and used 
Docker Compose to orchestrate both the web and Redis services together in a 
multi-container setup. I also learned about container networking, port mapping 
(8000:5000), and how services communicate using service names as hostnames 
inside a Docker network.

## Prerequisites
- Docker Desktop installed and running
- Git installed
- Python (optional, for local testing)

## Steps to Run

1. Clone the repo:
```bash
git clone https://github.com/gmakkena9/docker-lab-itcs6190.git
cd docker-lab-itcs6190
```

2. Build and run all services:
```bash
docker compose up
```

3. Open your browser and go to:
```
http://localhost:8000
```

4. Refresh the page a few times — the counter increments with each visit.

5. To stop the containers:
```bash
Ctrl+C
```

## Project Structure
- `app.py` — Flask web app with Redis hit counter
- `Dockerfile` — Containerizes the Python app using python:3.7-alpine
- `compose.yaml` — Defines web and redis services with Docker Compose
- `requirements.txt` — Python dependencies (flask, redis)
- `screenshots.docx` — Screenshots of Docker Desktop and browser output

## Services
| Service | Image | Port |
|---------|-------|------|
| web | Built from Dockerfile | 8000:5000 |
| redis | redis:alpine | default |

## Errors Logged
Three intentional and observed errors were logged as GitHub Issues:
1. `404 error for /favicon.ico`
2. `Redis running without authentication`
3. `Flask running on development server`

## References
- [Docker CLI Cheat Sheet](https://docs.docker.com/get-started/docker_cheatsheet.pdf)
- [GitHub Markdown Guide](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
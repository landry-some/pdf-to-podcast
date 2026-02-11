# AI Web App (Gradio + FastAPI)

This project is a containerized AI-powered web application built with Python, Gradio, and a production-ready ASGI server (Uvicorn). It provides an interactive UI for working with AI models and supports deployment via Docker and Docker Compose.

---

## Features

- Interactive web UI powered by Gradio
- Backend served with Uvicorn (ASGI)
- Docker and Docker Compose support
- Environment-based API key configuration
- Static file serving support
- Example configurations included

---

## Tech Stack

- Python
- Gradio
- FastAPI / ASGI
- Uvicorn
- Docker
- Docker Compose

---

## Installation (Local Development)

Clone the repository:

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Or if using `pyproject.toml`:

```bash
pip install .
```

---

## Running Locally

Set your API key (example for OpenAI):

```bash
export OPENAI_API_KEY=your_api_key_here
```

Start the application:

```bash
python main.py
```

Or using Uvicorn directly:

```bash
uvicorn main:app --host 0.0.0.0 --port 8000
```

---

## Running with Docker

Build and run with Docker Compose:

```bash
docker-compose up --build
```

Or build manually:

```bash
docker build -t ai-web-app .
docker run -p 8000:8000 ai-web-app
```

---

## Project Structure Overview

- `main.py` – Application entry point  
- `static/` – Static assets  
- `examples/` – Example usage configurations  
- `Dockerfile` – Container build configuration  
- `docker-compose.yml` – Multi-service deployment setup  
- `pyproject.toml` – Python dependency configuration  

---

## Environment Variables

Configure required API keys via environment variables:

- `OPENAI_API_KEY`
- Any other provider keys used in the app

Never commit API keys to source control.

---

## Deployment

This project is production-ready with:

- ASGI server (Uvicorn)
- Docker containerization
- Environment-based configuration
- Static file handling

It can be deployed to:

- VPS servers
- Cloud platforms (AWS, GCP, Azure)
- Container platforms (Fly.io, Railway, Render, etc.)

---

# AGENTS

This repository provides a Docker Compose stack for running Ollama together with Open WebUI.

## Build and Run

1. Install Python dependencies:
   ```sh
   pip install -r requirements.txt
   ```
2. Start the services:
   ```sh
   docker compose up -d
   ```

## Guidelines

- Keep `README.md`, `requirements.txt`, and `docker-compose.yml` consistent.
- Exposed ports: 11434 for Ollama and 3000 for Open WebUI.
- Use two spaces for indentation in YAML and Markdown files.

## Testing

- Run `docker compose config` to validate compose files before committing.


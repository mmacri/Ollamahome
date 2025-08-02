# Ollama Home

This repository provides a Docker Compose configuration for running [Ollama](https://ollama.ai) together with [Open WebUI](https://github.com/open-webui/open-webui). The stack exposes both services on your local network so you can host an AI chat interface at home.

## Requirements

- Docker Desktop on Windows 11 with the WSL2 backend.
- Python 3.8+ with `pip`.
- Install Python dependencies:
  ```sh
  pip install -r requirements.txt
  ```
- Optional: an NVIDIA GPU with drivers and the NVIDIA Container Toolkit for hardware acceleration.

## Usage

1. Start the services:
   ```sh
   docker compose up -d
   ```
2. Open your browser to `http://localhost:3000` to access Open WebUI.
   - From other devices on your network, replace `localhost` with the IP address of this PC.
3. The Ollama API is available on port `11434` for programmatic access.

### Managing models

Use the Open WebUI interface or run commands inside the `ollama` container, for example:

```sh
docker exec -it ollama ollama run llama3
```

### Stopping

```sh
docker compose down
```

## Optional configuration

- To persist data, volumes are created for both Ollama and Open WebUI.
- GPU acceleration can be enabled by configuring Docker to expose your GPU (e.g. `--gpus all` or setting `NVIDIA_VISIBLE_DEVICES=all`).
- Ports can be adjusted in `docker-compose.yml` if needed.


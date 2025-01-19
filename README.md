# my-ChatGPT

## Ollama using Docker Compose

```bash
version: '3.8'
services:
  ollama:
    image: ollama/ollama:latest
    container_name: ollama
    ports:
      - "11434:11434"
    volumes:
      - ./ollama:/root/.ollama
    restart: unless-stopped
    command: serve
```
Create a docker-compose.yml file with above content

```bash
docker-compose up --bulid -d
```
Access olama on the exposed port.

## To load Model using olama docker 

- get inside Ollama docker 

```bash
docker exec -it ollama /bin/bash 
```
- pull and load a model 

```bash
ollama pull llama3.2:1b

```

## my-ChatGPT
```bash
docker-compose up --bulid -d
```

**goto** [http://localhost:3000](http://localhost:3000)
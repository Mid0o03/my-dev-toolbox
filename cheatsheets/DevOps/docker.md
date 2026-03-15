# Docker Cheatsheet

## Basic Commands
- `docker build -t image_name .`: Build an image from a Dockerfile.
- `docker run -p 3000:3000 image_name`: Run a container.
- `docker ps`: List running containers.
- `docker ps -a`: List all containers.
- `docker stop container_id`: Stop a container.
- `docker rm container_id`: Remove a container.
- `docker images`: List images.
- `docker rmi image_id`: Remove an image.
- `docker logs container_id`: View logs.
- `docker exec -it container_id /bin/sh`: Open a shell in a container.

## Docker Compose
- `docker-compose up`: Start services.
- `docker-compose up -d`: Start services in background.
- `docker-compose down`: Stop and remove services.
- `docker-compose logs -f`: Follow logs.

## Dockerfile Example
```dockerfile
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["npm", "start"]
```

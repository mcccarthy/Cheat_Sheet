
# Docker Cheat Sheet

## What is Docker?

**Docker** is a platform that allows developers to package, deploy, and run applications inside containers. Containers are lightweight, portable, and isolated from the host system.

---

## Basic Docker Commands

### 1. Docker Version & Info

- **Check Docker version**:

  ```bash
  docker --version
  ```

- **Get detailed system info**:

  ```bash
  docker info
  ```

### 2. Docker Images

- **List all images**:

  ```bash
  docker images
  ```

- **Pull an image from Docker Hub**:

  ```bash
  docker pull <image_name>
  ```

  Example:

  ```bash
  docker pull nginx
  ```

- **Remove an image**:

  ```bash
  docker rmi <image_name>
  ```

### 3. Docker Containers

- **List running containers**:

  ```bash
  docker ps
  ```

- **List all containers (running and stopped)**:

  ```bash
  docker ps -a
  ```

- **Run a container**:

  ```bash
  docker run <image_name>
  ```

  Example (run and expose port):

  ```bash
  docker run -d -p 8080:80 nginx
  ```

- **Run a container with a custom name**:

  ```bash
  docker run --name <container_name> <image_name>
  ```

- **Stop a running container**:

  ```bash
  docker stop <container_name>
  ```

- **Remove a stopped container**:

  ```bash
  docker rm <container_name>
  ```

- **Start an existing container**:

  ```bash
  docker start <container_name>
  ```

- **Restart a container**:

  ```bash
  docker restart <container_name>
  ```

- **Remove all stopped containers**:

  ```bash
  docker container prune
  ```

### 4. Docker Logs & Stats

- **View logs of a container**:

  ```bash
  docker logs <container_name>
  ```

- **Monitor resource usage (CPU, Memory, etc.)**:

  ```bash
  docker stats
  ```

### 5. Docker Networks

- **List all networks**:

  ```bash
  docker network ls
  ```

- **Create a new network**:

  ```bash
  docker network create <network_name>
  ```

- **Connect a container to a network**:

  ```bash
  docker network connect <network_name> <container_name>
  ```

---

## Writing Dockerfiles

A **Dockerfile** is a text document that contains all the commands needed to build a Docker image.

### Sample Dockerfile

```dockerfile
# Use a base image
FROM node:14

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and install dependencies
COPY package.json .
RUN npm install

# Copy the rest of the app’s code into the container
COPY . .

# Expose a port
EXPOSE 3000

# Define the default command to run the app
CMD ["npm", "start"]
```

### Key Dockerfile Instructions

- **FROM**: Specifies the base image to use (e.g., `node`, `alpine`, etc.).
- **WORKDIR**: Sets the working directory inside the container.
- **COPY**: Copies files from the host to the container.
- **RUN**: Executes commands inside the container, often used to install dependencies.
- **EXPOSE**: Informs Docker that the container will listen on a specific port.
- **CMD**: Defines the default command that runs when the container starts.

### Dockerfile Best Practices

- Use specific versions for base images (e.g., `node:14` instead of `node:latest`).
- Minimize the number of `RUN` commands to keep image layers small.
- Use `.dockerignore` to exclude unnecessary files from the build context (similar to `.gitignore`).

---

## Container Management

### 1. Build and Run Docker Containers

- **Build an image from a Dockerfile**:

  ```bash
  docker build -t <image_name> .
  ```

  Example:

  ```bash
  docker build -t my-app .
  ```

- **Run a container from the built image**:

  ```bash
  docker run -d -p 3000:3000 my-app
  ```

### 2. Docker Volumes

- **List all volumes**:

  ```bash
  docker volume ls
  ```

- **Create a volume**:

  ```bash
  docker volume create <volume_name>
  ```

- **Mount a volume to a container**:

  ```bash
  docker run -d -v <volume_name>:/path/in/container <image_name>
  ```

  Example:

  ```bash
  docker run -d -v my-volume:/app my-app
  ```

- **Remove a volume**:

  ```bash
  docker volume rm <volume_name>
  ```

### 3. Docker Compose

**Docker Compose** is a tool for defining and running multi-container Docker applications using a `.yml` file.

#### Sample `docker-compose.yml`

```yaml
version: '3'
services:
  web:
    image: nginx
    ports:
      - "8080:80"
  app:
    build: .
    ports:
      - "3000:3000"
    volumes:
      - .:/app
    depends_on:
      - db
  db:
    image: postgres
    environment:
      POSTGRES_USER: user
      POSTGRES_PASSWORD: password
```

### Common Docker Compose Commands

- **Start services defined in `docker-compose.yml`**:

  ```bash
  docker-compose up
  ```

- **Run in detached mode**:

  ```bash
  docker-compose up -d
  ```

- **Stop services**:

  ```bash
  docker-compose down
  ```

- **View logs from services**:

  ```bash
  docker-compose logs
  ```

---

## Docker Registry & Images

### 1. Push and Pull Images from Docker Hub

- **Log in to Docker Hub**:

  ```bash
  docker login
  ```

- **Tag an image**:

  ```bash
  docker tag <image_name> <dockerhub_username>/<repo_name>:<tag>
  ```

  Example:

  ```bash
  docker tag my-app havoc/my-app:v1.0
  ```

- **Push an image to Docker Hub**:

  ```bash
  docker push <dockerhub_username>/<repo_name>:<tag>
  ```

- **Pull an image from Docker Hub**:

  ```bash
  docker pull <dockerhub_username>/<repo_name>:<tag>
  ```

### 2. Clean Up Docker

- **Remove unused images**:

  ```bash
  docker image prune
  ```

- **Remove all unused containers, networks, and volumes**:

  ```bash
  docker system prune
  ```

---

This should now be a working and clean Markdown file with no unnecessary syntax errors. Let me know if you encounter any further issues!

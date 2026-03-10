# Docker Command Reference

Docker is a containerization platform that allows developers to package applications and their dependencies into lightweight, portable containers. These containers can run consistently across development, testing, and production environments.

Docker is widely used in modern **DevOps workflows**, CI/CD pipelines, and microservices architectures.

---

# Table of Contents

1. Introduction to Docker
2. Docker Architecture
3. Docker Setup and Information
4. Image Management
5. Container Management
6. Volume Management
7. Networking
8. Docker Compose
9. Dockerfile Essentials
10. Best Practices
11. Cleanup Commands
12. Common Workflow Example
13. Additional Resources

---

# Introduction to Docker

Docker solves the classic problem of **"It works on my machine"** by packaging applications along with all dependencies into containers.

Key advantages of Docker include:

* Environment consistency
* Lightweight virtualization
* Faster application deployment
* Improved resource utilization
* Simplified DevOps workflows

---

# Docker Architecture

Docker follows a **client-server architecture**.

Main components include:

### Docker Client

The Docker client is the command-line interface used to interact with Docker.

Example:

```bash
docker run nginx
```

The command is sent to the Docker daemon.

### Docker Daemon

The Docker daemon (`dockerd`) runs in the background and is responsible for:

* Building images
* Running containers
* Managing networks
* Managing volumes

### Docker Images

Images are **read-only templates** used to create containers.

Example:

```
nginx image
node image
ubuntu image
```

### Docker Containers

Containers are **running instances of Docker images**.

They are isolated environments that contain:

* Application code
* Runtime
* System libraries
* Dependencies

---

# Docker Setup and Information

| Command            | Description                                   |
| ------------------ | --------------------------------------------- |
| `docker --version` | Displays the installed Docker version         |
| `docker info`      | Shows detailed system-wide Docker information |
| `docker help`      | Lists all available Docker commands           |

---

# Image Management

| Command                                      | Description                               |
| -------------------------------------------- | ----------------------------------------- |
| `docker images`                              | Lists all locally available Docker images |
| `docker pull <image>`                        | Downloads an image from Docker Hub        |
| `docker rmi <image>`                         | Removes a Docker image                    |
| `docker image inspect <image>`               | Displays detailed image information       |
| `docker image prune`                         | Removes unused images                     |
| `docker build -t <image_name> .`             | Builds an image from a Dockerfile         |
| `docker tag <source_image> <repository:tag>` | Assigns a new tag to an existing image    |

Example:

```bash
docker build -t my-node-app .
```

---

# Container Management

| Command                                 | Description                             |
| --------------------------------------- | --------------------------------------- |
| `docker ps`                             | Lists running containers                |
| `docker ps -a`                          | Lists all containers                    |
| `docker run <image>`                    | Creates and starts a container          |
| `docker run -it <image>`                | Runs container interactively            |
| `docker run -d <image>`                 | Runs container in background            |
| `docker run --name <name> <image>`      | Runs container with custom name         |
| `docker exec -it <container> /bin/bash` | Access container shell                  |
| `docker start <container>`              | Start a stopped container               |
| `docker stop <container>`               | Stop a container                        |
| `docker restart <container>`            | Restart container                       |
| `docker rm <container>`                 | Remove container                        |
| `docker logs <container>`               | View container logs                     |
| `docker inspect <container>`            | Display container details               |
| `docker stats`                          | Show real-time container resource usage |

---

# Volume Management

Volumes allow persistent storage for container data.

| Command                                                  | Description                   |
| -------------------------------------------------------- | ----------------------------- |
| `docker volume create <volume_name>`                     | Create a new volume           |
| `docker volume ls`                                       | List all volumes              |
| `docker volume inspect <volume_name>`                    | Inspect volume details        |
| `docker volume rm <volume_name>`                         | Remove volume                 |
| `docker run -v <volume_name>:/path/in/container <image>` | Mount volume inside container |

Example:

```bash
docker run -v myvolume:/data ubuntu
```

---

# Networking

Docker networking enables communication between containers.

| Command                                       | Description                 |
| --------------------------------------------- | --------------------------- |
| `docker network ls`                           | List networks               |
| `docker network create <network_name>`        | Create network              |
| `docker network inspect <network_name>`       | Show network details        |
| `docker network rm <network_name>`            | Remove network              |
| `docker run --network <network_name> <image>` | Attach container to network |

Example:

```bash
docker network create mynetwork
```

---

# Docker Compose

Docker Compose is used for **multi-container applications**.

Example `docker-compose.yml`:

```yaml
version: '3'

services:
  web:
    image: nginx
    ports:
      - "80:80"

  database:
    image: mysql
```

Commands:

| Command                | Description              |
| ---------------------- | ------------------------ |
| `docker compose up`    | Start services           |
| `docker compose up -d` | Start in detached mode   |
| `docker compose down`  | Stop and remove services |
| `docker compose ps`    | List running services    |
| `docker compose logs`  | View service logs        |
| `docker compose build` | Build services           |

---

# Dockerfile Essentials

Example Dockerfile:

```dockerfile
FROM node:18

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "start"]
```

Important Dockerfile instructions:

| Instruction | Description           |
| ----------- | --------------------- |
| `FROM`      | Base image            |
| `WORKDIR`   | Set working directory |
| `COPY`      | Copy files            |
| `RUN`       | Execute commands      |
| `EXPOSE`    | Declare port          |
| `CMD`       | Default command       |

---

# Docker Best Practices

For production environments, follow these best practices:

1. Use **official base images**
2. Keep images **small and optimized**
3. Use **multi-stage builds**
4. Avoid running containers as **root**
5. Use **.dockerignore** to reduce build size
6. Tag images with versions
7. Use **environment variables for configuration**

Example `.dockerignore`:

```
node_modules
.git
.env
logs
```

---

# Common Docker Workflow

Typical development workflow:

1. Write a Dockerfile
2. Build the image

```bash
docker build -t myapp .
```

3. Run the container

```bash
docker run -p 3000:3000 myapp
```

4. Verify container

```bash
docker ps
```

---

# Cleanup Commands

| Command                  | Description                                |
| ------------------------ | ------------------------------------------ |
| `docker system prune`    | Remove unused containers, networks, images |
| `docker container prune` | Remove stopped containers                  |
| `docker image prune`     | Remove unused images                       |
| `docker volume prune`    | Remove unused volumes                      |

---

# Additional Resources

Docker Documentation
[https://docs.docker.com/](https://docs.docker.com/)

Docker Hub
[https://hub.docker.com/](https://hub.docker.com/)

Docker Compose Documentation
[https://docs.docker.com/compose/](https://docs.docker.com/compose/)

Add a Star⭐ if you find this Repository Helpful !!

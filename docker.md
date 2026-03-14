# Docker Command Reference

Docker is a containerization platform that allows developers to package applications and their dependencies into lightweight, portable containers. These containers can run consistently across development, testing, and production environments.

A container includes everything required to run an application such as libraries, runtime, and system tools. This makes applications portable across different systems.

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

A container ensures that the same environment runs everywhere, which eliminates inconsistencies between development, testing, and production systems.

Key advantages of Docker include:

* Environment consistency
* Lightweight virtualization
* Faster application deployment
* Improved resource utilization
* Simplified DevOps workflows

Example:

Suppose a developer builds a Node.js application that works correctly on their laptop but fails on the production server due to different library versions. By packaging the application inside a Docker container, the exact environment can be replicated on any machine.

Example command:

```bash
docker run nginx
```

This command downloads the nginx image (if not already present) and starts a container running the nginx web server.

---

# Docker Architecture

Docker follows a **client-server architecture**.

The Docker client communicates with the Docker daemon, which performs the heavy work of building, running, and managing containers.

Main components include:

### Docker Client

The Docker client is the command-line interface used to interact with Docker. It sends commands to the Docker daemon.

Example:

```bash
docker run nginx
```

Here, the Docker client sends the request to start an nginx container.

---

### Docker Daemon

The Docker daemon (`dockerd`) runs in the background and is responsible for managing Docker objects such as images, containers, networks, and volumes.

Responsibilities of the Docker daemon include:

* Building images from Dockerfiles
* Creating and running containers
* Managing networking between containers
* Handling persistent storage through volumes

Example:

When the following command is executed:

```bash
docker build -t myapp .
```

The Docker daemon reads the Dockerfile and builds the image.

---

### Docker Images

Images are **read-only templates** used to create containers. They contain the application code, runtime, system libraries, and dependencies required to run an application.

Images are built from Dockerfiles and stored in container registries such as Docker Hub.

Example images:

```
nginx
node
ubuntu
mysql
```

Example command:

```bash
docker pull ubuntu
```

This command downloads the Ubuntu image from Docker Hub.

---

### Docker Containers

Containers are **running instances of Docker images**.

A container provides an isolated environment where applications can run without interfering with the host system or other containers.

Containers are lightweight compared to virtual machines because they share the host operating system kernel.

Example:

```bash
docker run -it ubuntu
```

This command starts an interactive Ubuntu container.

---

# Docker Setup and Information

The following commands help verify Docker installation and display system information.

| Command            | Description                                   |
| ------------------ | --------------------------------------------- |
| `docker --version` | Displays the installed Docker version         |
| `docker info`      | Shows detailed system-wide Docker information |
| `docker help`      | Lists all available Docker commands           |

Example:

```bash
docker --version
```

Output example:

```
Docker version 25.0.3, build abc123
```

---

# Image Management

Docker images are used to create containers. These commands help manage images locally.

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

This command builds a Docker image named **my-node-app** using the Dockerfile in the current directory.

---

# Container Management

Containers are the runtime instances of Docker images.

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

Example:

```bash
docker run -d -p 80:80 nginx
```

This command runs the nginx container in detached mode and maps port 80 of the container to port 80 of the host.

---

# Volume Management

Volumes allow containers to store persistent data even after containers are removed.

Without volumes, container data is lost when the container stops.

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

This command mounts the volume **myvolume** inside the container at `/data`.

---

# Networking

Docker networking allows containers to communicate with each other and with external systems.

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

This command creates a custom Docker network where containers can communicate securely.

---

# Docker Compose

Docker Compose is a tool used to define and run **multi-container applications** using a YAML configuration file.

It allows developers to start multiple services with a single command.

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

Example:

```bash
docker compose up -d
```

This command starts all services defined in the compose file.

---

# Dockerfile Essentials

A Dockerfile is a text file that contains instructions to build a Docker image.

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

| Instruction | Description                          |
| ----------- | ------------------------------------ |
| `FROM`      | Defines the base image               |
| `WORKDIR`   | Sets the working directory           |
| `COPY`      | Copies files from host to container  |
| `RUN`       | Executes commands during image build |
| `EXPOSE`    | Declares container port              |
| `CMD`       | Specifies default container command  |

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

This prevents unnecessary files from being included in the Docker image.

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

This workflow ensures that applications are packaged, deployed, and tested consistently.

---

# Cleanup Commands

| Command                  | Description                                |
| ------------------------ | ------------------------------------------ |
| `docker system prune`    | Remove unused containers, networks, images |
| `docker container prune` | Remove stopped containers                  |
| `docker image prune`     | Remove unused images                       |
| `docker volume prune`    | Remove unused volumes                      |

Example:

```bash
docker system prune
```

This command removes unused Docker resources to free disk space.

---

# Additional Resources

Docker Documentation
[https://docs.docker.com/](https://docs.docker.com/)

Docker Hub
[https://hub.docker.com/](https://hub.docker.com/)

Docker Compose Documentation
[https://docs.docker.com/compose/](https://docs.docker.com/compose/)

Add a Star⭐ if you find this repository helpful.

## 🐳 Docker Basic Commands

Docker is one of the most essential tools in DevOps for containerizing applications.  
Here’s a list of useful **Docker commands**, neatly categorized for your DevOps learning journey.

---

### Docker Setup & Information
| Command | Description |
|----------|-------------|
| `docker --version` | Check Docker version |
| `docker info` | Display system-wide Docker information |
| `docker help` | Show help for Docker commands |

---

### Images Management
| Command | Description |
|----------|-------------|
| `docker images` | List all local images |
| `docker pull <image>` | Download image from Docker Hub |
| `docker rmi <image>` | Remove an image |
| `docker image inspect <image>` | Display detailed image information |
| `docker image prune` | Remove unused images |
| `docker build -t <image_name> .` | Build image from Dockerfile |
| `docker tag <source_image> <repo:tag>` | Tag an image with a name and version |

---

### Container Management
| Command | Description |
|----------|-------------|
| `docker ps` | List running containers |
| `docker ps -a` | List all containers (including stopped ones) |
| `docker run <image>` | Run a container from an image |
| `docker run -it <image>` | Run container interactively with terminal |
| `docker run -d <image>` | Run container in detached mode (background) |
| `docker run --name <name> <image>` | Run container with a custom name |
| `docker exec -it <container> /bin/bash` | Access running container shell |
| `docker start <container>` | Start a stopped container |
| `docker stop <container>` | Stop a running container |
| `docker restart <container>` | Restart container |
| `docker rm <container>` | Remove a stopped container |
| `docker logs <container>` | View container logs |
| `docker inspect <container>` | View container details |
| `docker stats` | Show real-time resource usage by containers |

---

### Volumes (Data Persistence)
| Command | Description |
|----------|-------------|
| `docker volume create <volume_name>` | Create a new volume |
| `docker volume ls` | List all volumes |
| `docker volume inspect <volume_name>` | Display volume details |
| `docker volume rm <volume_name>` | Remove a volume |
| `docker run -v <volume_name>:/path/in/container <image>` | Mount a volume to a container |

---

### Networking
| Command | Description |
|----------|-------------|
| `docker network ls` | List all networks |
| `docker network create <network_name>` | Create a custom network |
| `docker network inspect <network_name>` | Show network details |
| `docker network rm <network_name>` | Remove a network |
| `docker run --network <network_name> <image>` | Attach container to a network |

---

### Docker Compose
| Command | Description |
|----------|-------------|
| `docker compose up` | Start services defined in `docker-compose.yml` |
| `docker compose up -d` | Start services in detached mode |
| `docker compose down` | Stop and remove all containers defined in compose file |
| `docker compose ps` | List running services |
| `docker compose logs` | Show logs of all services |
| `docker compose build` | Build or rebuild services |

---

### Cleanup Commands
| Command | Description |
|----------|-------------|
| `docker system prune` | Remove unused containers, images, and networks |
| `docker container prune` | Remove all stopped containers |
| `docker image prune` | Remove dangling (unused) images |
| `docker volume prune` | Remove unused volumes |

---

### Dockerfile Essentials

A basic **Dockerfile** example:
```dockerfile
# Use base image
FROM node:18

# Set working directory
WORKDIR /app

# Copy files
COPY . .

# Install dependencies
RUN npm install

# Expose port
EXPOSE 3000

# Start application
CMD ["npm", "start"]

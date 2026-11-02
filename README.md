# 🐳 Docker Practice Repository

Welcome to my Docker Practice Repository!

This repository contains my hands-on practice, notes, and implementations of essential Docker concepts and commands. The objective is to understand containerization, build Docker images, manage containers, configure networking, and work with persistent storage.

## 📚 Topics Covered

- Docker Fundamentals
- Docker Architecture
- Docker Installation and Configuration
- Docker Images
- Docker Containers
- Dockerfile Instructions
- Docker Volumes
- Docker Networking
- Docker Compose
- Environment Variables
- Multi-Stage Docker Builds
- Container Troubleshooting
- Docker Registry and Docker Hub

## 🛠️ Docker Commands

### 1. Docker Version and Information

```bash
docker --version
docker version
docker info
```

### 2. Docker Images

```bash
docker images
docker pull nginx
docker build -t my-image .
docker rmi image-name
docker image inspect image-name
```

### 3. Docker Containers

```bash
docker ps
docker ps -a
docker run -d nginx
docker run -it ubuntu bash
docker stop container-id
docker start container-id
docker restart container-id
docker rm container-id
docker logs container-id
docker inspect container-id
docker exec -it container-id bash
```

### 4. Dockerfile Instructions

| Instruction | Description |
|---|---|
| FROM | Defines the base image |
| WORKDIR | Sets the working directory |
| COPY | Copies files from host to image |
| ADD | Copies files and supports additional features |
| RUN | Executes commands during image build |
| CMD | Defines the default command |
| ENTRYPOINT | Configures the main executable |
| EXPOSE | Documents the container port |
| ENV | Sets environment variables |
| ARG | Defines build-time variables |
| USER | Specifies the user to run commands |
| VOLUME | Defines mount points |
| LABEL | Adds metadata to an image |

### 5. Docker Build and Run

```bash
docker build -t myapp .
docker run -d -p 8080:80 myapp
docker run -d --name mycontainer nginx
docker run -d --restart always nginx
```

### 6. Docker Port Mapping

```bash
docker run -d -p 8080:80 nginx
docker port container-id
```

Host Port: 8080  
Container Port: 80

### 7. Docker Volumes

```bash
docker volume ls
docker volume create myvolume
docker volume inspect myvolume
docker volume rm myvolume
docker run -d -v myvolume:/data nginx
```

### 8. Docker Networking

```bash
docker network ls
docker network create mynetwork
docker network inspect mynetwork
docker network connect mynetwork container-id
docker network disconnect mynetwork container-id
docker network rm mynetwork
```

### 9. Docker Compose

```bash
docker compose up -d
docker compose down
docker compose ps
docker compose logs
docker compose build
docker compose restart
```

### 10. Docker Hub

```bash
docker login
docker tag myapp username/myapp:latest
docker push username/myapp:latest
docker pull username/myapp:latest
```

### 11. Docker Cleanup

```bash
docker system df
docker container prune
docker image prune
docker volume prune
docker network prune
docker system prune
```

**Note:** Cleanup commands can delete unused Docker resources. Review what will be removed before executing them.

## 🏗️ Docker Architecture

Docker follows a client-server architecture.

- **Docker Client:** Accepts commands from users.
- **Docker Daemon:** Manages images, containers, networks, and volumes.
- **Docker Images:** Read-only templates used to create containers.
- **Docker Containers:** Running instances of Docker images.
- **Docker Registry:** Stores and distributes Docker images.

## 📂 Repository Structure

```text
docker-practice/
│
├── README.md
│
├── docker-basics/
│   └── commands.md
│
├── dockerfiles/
│   ├── Dockerfile
│   └── multistage.Dockerfile
│
├── docker-compose/
│   └── docker-compose.yml
│
├── networking/
│
├── volumes/
│
└── projects/
```

*The directory structure represents the recommended organization for this repository.*

## 🎯 Practical Learning Objectives

Through this repository, I aim to:

1. Understand how Docker works internally.
2. Build and manage custom Docker images.
3. Containerize applications.
4. Connect multiple containers using Docker networking.
5. Persist application data using Docker volumes.
6. Deploy multi-container applications using Docker Compose.
7. Optimize Docker images using multi-stage builds.
8. Troubleshoot real-world container issues.

## 🚀 Next Steps

- Advanced Docker concepts
- Docker security best practices
- Docker image optimization
- Kubernetes integration
- CI/CD pipeline integration using Jenkins

## 👨‍💻 Author

Maintained as part of my hands-on DevOps practice and technical documentation.

**Learning by doing. Practising by building. Improving through implementation.**

---
⭐ If you find this repository useful, feel free to explore the examples and practice along!

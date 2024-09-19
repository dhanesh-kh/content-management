# Docker Guide

This guide provides an introduction to Docker, focusing on basic commands and usage.

## What is Docker?
Docker is a platform that allows developers to build, test, and deploy applications in isolated containers. Key features include:
- **Containerization**: Package applications and their dependencies for consistent deployment across environments.
- **Auto Scaling**: Dynamically scale containers for load balancing and improved performance.

## What is a Docker Image?
A Docker image is a lightweight, standalone, and executable software package that includes everything needed to run an application. Key features of Docker images:
- **Immutability**: Docker images are read-only and cannot be altered after creation.
- **Portability**: Docker images can be shared across different environments, ensuring consistent application behavior.

## Docker Commands

### Logging into Docker Hub
Authenticate with Docker Hub from the command line:
```bash
docker login
```
Enter your Docker Hub username and password.

### Starting Services
To start all services defined in a `docker-compose.yml` file:
```bash
docker-compose up -d
```
This starts the containers in detached mode.

### Resetting the Testing Environment
To stop services, remove volumes, and restart:
1. Stop services and remove volumes:
    ```bash
    docker-compose down -v
    ```
2. Restart services:
    ```bash
    docker-compose up -d
    ```

### Viewing Logs
To view and follow logs from containers:
```bash
docker-compose logs -f
```

### Shutting Down Services
To stop and remove all running containers:
```bash
docker-compose down
```

## Docker Images

### Building Images
To build a Docker image based on the `Dockerfile`:
```bash
docker-compose build
```

### Tagging and Pushing Images to Docker Hub

1. **Tagging**: Tag your local image for Docker Hub:
    ```bash
    docker tag local-image:tagname username/repository:tag
    ```
    Example:
    ```bash
    docker tag myapp:latest john/myapp:latest
    ```

2. **Pushing**: Push the tagged image to Docker Hub:
    ```bash
    docker push username/repository:tag
    ```
    Example:
    ```bash
    docker push john/myapp:latest
    ```
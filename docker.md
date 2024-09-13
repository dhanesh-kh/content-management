# Docker Guide

This is a guide to Docker for newcomers interested to learn about the platform. 


## <ins> What is Docker? <ins>

- A platform where you can build, test, download, and deploy applications in containers.
- Quick auto scaling: Dynamically scale containers for load balancing and performance improvement. 

## <ins> What is a Container & Containerization? <ins> 
- A container is like a virtual machine, except it doesn't virtualize a whole hardware machine and rather is a software package with dependencies needed to execute software appliciations.

## <ins> What is Vertical & Horizontal Scaling in Docker? <ins> 

- Scaling is adjusting the number of containers or power of a machine to balance loads for particular tasks/projects. 
- <u>Vertical Scaling</u> means to add more power to your current machines through upgrading hardware components to improve capabilities.
- <u>Horizontal Scaling </u> means to add more machines to help balance the workload or handle an increased workload.  

##  What is Virtualization?  

- Virtualization is creating a virtual copy of an entire hardware machine on your own machine. For example, running an Ubuntu OS instance on your Windows computer using VirtualBox.

## What is a Thread?

- A thread is a set of instructions sent to the CPU to execute. Threading is the process of sending instructions to the CPU to execute. 
 
Test 2
# Docker Setup

## Prerequisites
- Ensure Docker and Docker Compose are installed on your computer.

### Creating a Docker Hub Account
- Visit [Docker Hub](https://hub.docker.com/) and sign up for an account.
- Once registered, you can create repositories to store your Docker images.

### Logging into Docker Hub from the Command Line
- **`docker login`**
- Enter your Docker Hub username and password.

### Starting the Services
- To start all services defined in the Docker Compose file, navigate to the directory containing your `docker-compose.yml` file and run:
  - **`docker-compose up -d`**
  - This command starts the containers in the background.

## Resetting the Testing Environment
- If you need to reset your environment, e.g., to clear test data:
  - **Stop all services and remove volumes**:
    - **`docker-compose down -v`**
  - **Restart the services**:
    - **`docker-compose up -d`**

### Viewing Logs
- To view logs for troubleshooting or monitoring application behavior:
  - **`docker-compose logs -f`**
  - The `-f` flag tails the log output.

### Shutting Down
- To stop and remove all running containers:
  - **`docker-compose down`**

## Docker Images

### Building Docker Images
- To build a Docker image for your application, ensure you have a Dockerfile in the same directory as your `docker-compose.yml`. Then run:
  - **`docker-compose build`**

## Pushing Images to Docker Hub

### Tagging Your Docker Image
- **`docker tag local-image:tagname username/repository:tag`**
  - For example:
    - **`docker tag myfastapi:latest john/myfastapi:latest`**

### Pushing the Image
- **`docker push username/repository:tag`**
  - For example:
    - **`docker push john/myfastapi:latest`**
>

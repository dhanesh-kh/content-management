# Docker Guide
This is a guide to Docker for newcomers interested to learn about the platform. 

## <ins> What is Docker? <ins>
- A platform where you can build, test, download, and deploy applications in containers.
- Quick auto scaling: Dynamically scale containers for load balancing and performance improvement. 
- Containerize applications for deployment and storage.

## Docker Usage

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


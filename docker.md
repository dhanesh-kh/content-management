# Docker Guide

This is a guide to Docker for newcomers interested to learn about the platform. 


## <ins> What is Docker? <ins>

- A platform where you can build, test, download, and deploy applications in containers.
- Quick auto scaling: Dynamically scale containers for load balancing and performance improvement. 
- 
## <ins> What is Kubernetes? <ins>
- Platform where containerized apps are managed, deployed, and scaled through automation. 
- Orchestrates clusters of virtual machines and tasks containers to run on those machines. 
- Makes workloads portable and run applications through multiple environments with consistency.   

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

## Why Choose Docker over Kubernetes?

- Simplicity: Easier, faster to use & setup. Requires less infrastructure & configuration compared to Kubernetes. Ideal for beginners or small scale projects

- Lower costs: Uses less resources. No complex orchestration. No vast clusters needed. 

- Rapid Prototyping: Quickly setup containers without worrying about orchestration

- Seamless CI/CD integration: Works well with CI/CD pipelines in much simpler manner than Kubernetes due to portability, efficiency, and lightweight nature

- Standalone Apps: Great for standalone apps on a single machine 
 
# Setup

## Prerequisites
- Ensure Docker and Docker Compose are installed on your computer.

### Creating a Docker Hub Account
- Visit [Docker Hub](https://hub.docker.com/) and sign up for an account.
- Once registered, you can create repositories to store your Docker images.

## Usage

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

# Install Windows Subsystem For Linux (WSL2) On Windows 10 & 11

## Prerequisites 

- Windows 10 version 2004 or higher or Windows 11
- Virtualization Enabled in BIOS
	- Restart PC & enter BIOS/UEFI settings by pressing F2,DEl, or ESC  during startup
	- Look for settings Intel VT-x or AMD-V and enable. 
	- Save settings & exit BIOS
- Internet connection with administrative priveleges
- Virtual machine platform (hyper-v) or virtualization on Windows enabled 

## Installation Procedure

- Open a terminal as Administrator (such as PowerShell)
- Type the command **`wsl --install`** and hit enter
- By default, Ubuntu distribution is installed
- Restart PC if needed
- Setup username & password for your Ubuntu distribution 
- Launch Ubuntu terminal by clicking dropdown option in your default terminal  
	
## Installation (macOS)

### Prerequisites

#### Mac with Intel chip
- [Docker Desktop for Mac with Intel chip](https://desktop.docker.com/mac/main/arm64/Docker.dmg?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-mac-arm64&_gl=1*3asmt6*_gcl_au*MTk4MjUzOTE5NC4xNzI2MDY0NjIz*_ga*MjEyMDgxMjcwMy4xNzI1NjMyNzQ4*_ga_XJWPQMJYHQ*MTcyNjY2ODQ3MS40LjEuMTcyNjY2ODUyNS42LjAuMA..)
- A supported version of macOS.
- At least 4 GB of RAM.
#### Mac with Apple silicon
- [Docker Desktop for Mac with Apple silicon](https://desktop.docker.com/mac/main/amd64/Docker.dmg?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-mac-amd64&_gl=1*t4tomt*_gcl_au*MTk4MjUzOTE5NC4xNzI2MDY0NjIz*_ga*MjEyMDgxMjcwMy4xNzI1NjMyNzQ4*_ga_XJWPQMJYHQ*MTcyNjY2ODQ3MS40LjEuMTcyNjY2ODUyNS42LjAuMA..)
- (optional) install Rosetta 2 for command line tools
- To install Rosetta 2 manually from the command line, run the following command:
  - **`softwareupdate --install-rosetta`**

### Install
- Download the installer using the download button for your respective processor.
- Double-click `Docker.dmg` to open the installer, then drag the Docker icon to the Applications folder. By default, Docker Desktop is installed at `/Applications/Docker.app`.
- Double-click `Docker.app` in the Applications folder to start Docker.
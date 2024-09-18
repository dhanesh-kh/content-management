# Docker Setup

### Prerequisites
- Ensure Docker and Docker Compose are installed on your computer.
    - [Windows](#installation-windows)
    - [MacOS](#installation-macos)

### Creating a Docker Hub Account
- Visit [Docker Hub](https://hub.docker.com/) and sign up for an account.
- Once registered, you can create repositories to store your Docker images.

## Installation (Windows) 
- Subsystem For Linux (WSL2) On Windows 10 & 11
- [Docker Desktop for Windows - x86_64](https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-win-amd64&_gl=1*ob2okp*_gcl_au*MTk4MjUzOTE5NC4xNzI2MDY0NjIz*_ga*MjEyMDgxMjcwMy4xNzI1NjMyNzQ4*_ga_XJWPQMJYHQ*MTcyNjY4MDQ2OC42LjEuMTcyNjY4MDQ4OS4zOS4wLjA.)
- [Docker Desktop for Windows - Arm (Beta)](https://desktop.docker.com/win/main/arm64/Docker%20Desktop%20Installer.exe?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-win-arm64&_gl=1*1sw13m4*_gcl_au*MTk4MjUzOTE5NC4xNzI2MDY0NjIz*_ga*MjEyMDgxMjcwMy4xNzI1NjMyNzQ4*_ga_XJWPQMJYHQ*MTcyNjY4MDQ2OC42LjEuMTcyNjY4MDQ4OS4zOS4wLjA.)

### Prerequisites 
- Windows 10 version 2004 or higher or Windows 11
- Virtualization Enabled in BIOS
	- Restart PC & enter BIOS/UEFI settings by pressing F2,DEl, or ESC  during startup
	- Look for settings Intel VT-x or AMD-V and enable. 
	- Save settings & exit BIOS
- Internet connection with administrative priveleges
- Virtual machine platform (hyper-v) or virtualization on Windows enabled 

### Installation Procedure
- Open a terminal as Administrator (such as PowerShell)
- Type the command **`wsl --install`** and hit enter
- By default, Ubuntu distribution is installed
- Restart PC if needed
- Setup username & password for your Ubuntu distribution 
- Launch Ubuntu terminal by clicking dropdown option in your default terminal  
	
## Installation (macOS)
- [Docker Desktop for Mac with Intel chip](https://desktop.docker.com/mac/main/arm64/Docker.dmg?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-mac-arm64&_gl=1*3asmt6*_gcl_au*MTk4MjUzOTE5NC4xNzI2MDY0NjIz*_ga*MjEyMDgxMjcwMy4xNzI1NjMyNzQ4*_ga_XJWPQMJYHQ*MTcyNjY2ODQ3MS40LjEuMTcyNjY2ODUyNS42LjAuMA..)
- [Docker Desktop for Mac with Apple silicon](https://desktop.docker.com/mac/main/amd64/Docker.dmg?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-mac-amd64&_gl=1*t4tomt*_gcl_au*MTk4MjUzOTE5NC4xNzI2MDY0NjIz*_ga*MjEyMDgxMjcwMy4xNzI1NjMyNzQ4*_ga_XJWPQMJYHQ*MTcyNjY2ODQ3MS40LjEuMTcyNjY2ODUyNS42LjAuMA..)
### Prerequisites

#### Mac with Intel chip
- A supported version of macOS.
- At least 4 GB of RAM.

#### Mac with Apple silicon
- (optional) install Rosetta 2 for command line tools
- To install Rosetta 2 manually from the command line, run the following command:
  - **`softwareupdate --install-rosetta`**

### Installation Procedure
- Download the installer using the download button for your respective processor.
- Double-click `Docker.dmg` to open the installer, then drag the Docker icon to the Applications folder. By default, Docker Desktop is installed at `/Applications/Docker.app`.
- Double-click `Docker.app` in the Applications folder to start Docker.
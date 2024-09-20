# Docker Setup

Docker setup involves creating a Docker Hub account, installing Docker Desktop,
and looking at prerequisites for Windows and/or macOS.

## Prerequisites

Ensure Docker and Docker Compose are installed on your computer. 
Follow the instructions for your specific operating system:

- [Windows Installation](#installation-windows)
- [macOS Installation](#installation-macos)

## Creating a Docker Hub Account

1. Visit [Docker Hub](https://hub.docker.com/) and sign up for an account.
2. After registration, you can create repositories to store your Docker images.

## Installation (Windows)

### Prerequisites (Windows)

- **Operating System**: Windows 10 version 2004 or higher, or Windows 11.
- **Virtualization**: Enable virtualization in BIOS/UEFI:
  - Restart your PC and enter BIOS/UEFI settings (press F2, DEL, or ESC during startup).
  - Enable Intel VT-x or AMD-V.
  - Save changes and exit BIOS.
- **Administrative Privileges**: 
Ensure you have an internet connection with administrative privileges.
- **Virtualization Platform**: 
Enable Hyper-V or another virtualization platform on Windows.

### Installation Procedure (Windows)

1. **Install WSL2**:
   - Open PowerShell as Administrator.
   - Run the command: `wsl --install`.
   - This installs the default Ubuntu distribution.
2. **Restart**: Restart your PC if prompted.
3. **Setup Ubuntu**:
   - Configure a username and password for Ubuntu.
4. **Launch Ubuntu**:
   - Open the Ubuntu terminal from the dropdown options in your default terminal.

### Docker Desktop Installers

- [Docker Desktop for Windows (x86_64)](https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-win-amd64&_gl=1*ob2okp*_gcl_au*MTk4MjUzOTE5NC4xNzI2MDY0NjIz*_ga*MjEyMDgxMjcwMy4xNzI1NjMyNzQ4*_ga_XJWPQMJYHQ*MTcyNjY4MDQ2OC42LjEuMTcyNjY4MDQ4OS4zOS4wLjA.)
- [Docker Desktop for Windows (Arm, Beta)](https://desktop.docker.com/win/main/arm64/Docker%20Desktop%20Installer.exe?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-win-arm64&_gl=1*1sw13m4*_gcl_au*MTk4MjUzOTE5NC4xNzI2MDY0NjIz*_ga*MjEyMDgxMjcwMy4xNzI1NjMyNzQ4*_ga_XJWPQMJYHQ*MTcyNjY4MDQ2OC42LjEuMTcyNjY4MDQ4OS4zOS4wLjA.)

![Docker for Windows Pictures](https://cdn.hashnode.com/res/hashnode/image/upload/v1627716953958/2F1xoBx1Y.png)

## Installation (macOS)

### Prerequisites (macOS)

- **Mac with Intel Chip**:
  - A supported version of macOS.
  - At least 4 GB of RAM.
- **Mac with Apple Silicon**:
  - (Optional) Install Rosetta 2 for command line tools:

  ```bash
  softwareupdate --install-rosetta
  ```

### Installation Procedure (macOS)

1. **Download Docker Desktop**:
   - Choose the installer for your processor:
     - [For Intel chips](https://desktop.docker.com/mac/main/amd64/Docker.dmg?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-mac-amd64&_gl=1*t4tomt*_gcl_au*MTk4MjUzOTE5NC4xNzI2MDY0NjIz*_ga*MjEyMDgxMjcwMy4xNzI1NjMyNzQ4*_ga_XJWPQMJYHQ*MTcyNjY2ODQ3MS40LjEuMTcyNjY2ODUyNS42LjAuMA..)
     - [For Apple Silicon](https://desktop.docker.com/mac/main/arm64/Docker.dmg?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-mac-arm64&_gl=1*3asmt6*_gcl_au*MTk4MjUzOTE5NC4xNzI2MDY0NjIz*_ga*MjEyMDgxMjcwMy4xNzI1NjMyNzQ4*_ga_XJWPQMJYHQ*MTcyNjY2ODQ3MS40LjEuMTcyNjY2ODUyNS42LjAuMA..)
2. **Install Docker**:
   - Double-click `Docker.dmg` to open the installer.
   - Drag the Docker icon to the Applications folder.
   Docker Desktop will be installed at `/Applications/Docker.app`.
3. **Start Docker**:
   - Double-click `Docker.app` in the Applications folder to start Docker.
![Docker For MACOS Picture](https://www.docker.com/wp-content/uploads/2021/04/docker-desktop-m1.jpg)
---

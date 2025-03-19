# Ansible Playbooks

This repository contains several Ansible playbooks to automate the installation and configuration of services.

## Playbook 1: Install and Configure Nginx

This playbook installs Nginx, checks if it's installed, clones a Git repository, and configures Nginx.

### Tasks:
1. **Install Nginx**
   - Installs the latest version of Nginx on the target machine.
2. **Check if Nginx is Installed**
   - Verifies if Nginx is successfully installed.
3. **Clone Git Repository**
   - Clones a specific Git repository to a predefined directory.
4. **Configure Nginx**
   - Configures Nginx by adding the necessary configuration files and restarting the service.

## Playbook 2: Install and Configure Docker

This playbook installs Docker, starts the Docker service, creates a Docker group, adds a user to the Docker group, and runs MySQL in a container.

### Tasks:
1. **Install Docker**
   - Installs Docker on the target machine.
2. **Start Docker Service**
   - Ensures the Docker service is started and enabled.
3. **Create Docker Group**
   - Creates a `docker` group to allow users to interact with Docker without `sudo`.
4. **Add User to Docker Group**
   - Adds the specified user to the `docker` group.
5. **Pull MySQL Docker Image**
   - Pulls the official MySQL Docker image from Docker Hub.
6. **Build Custom Docker Image**
   - Builds a custom Docker image from a provided Dockerfile.
7. **Create Docker Volume**
   - Creates a Docker volume to persist data.
8. **Create Docker Network**
   - Creates a custom Docker network for containers to communicate.
9. **Run MySQL Container**
   - Runs a MySQL container with the specified volume and network.

## Playbook 3: Install and Configure MySQL Server

This playbook installs MySQL, starts the MySQL service, and creates a database and user.

### Tasks:
1. **Install MySQL Server**
   - Installs the MySQL Server package.
2. **Start MySQL Service**
   - Ensures the MySQL service is started and enabled.
3. **Create MySQL Database**
   - Creates a specified database within MySQL.
4. **Create MySQL User**
   - Creates a new MySQL user and grants permissions to the newly created database.
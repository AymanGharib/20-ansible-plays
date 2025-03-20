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

## Playbook 4: (Not Defined Yet)

_(Add details here when Playbook 4 is defined.)_

## Playbook 5: Check if Apache is Running and Restart If Stopped

This playbook checks if the Apache service is running, gathers service facts, and restarts it if necessary.

### Tasks:
1. **Check if Apache is Running**
   - Checks if Apache is running using the `service` module.
2. **Gather Service Facts**
   - Collects service-related information.
3. **Restart Apache if Not Running**
   - Restarts Apache service if it is not running.

## Playbook 6: Create and Assign Users to Groups

This playbook creates users from a list and assigns them to corresponding groups based on the index.

### Tasks:
1. **Create Users**
   - Creates a list of users using a loop.
2. **Create Groups**
   - Creates a list of groups using a loop.
3. **Assign Users to Groups**
   - Assigns each user to the corresponding group, based on the index of the user and group.

## Playbook 7: Create a System Backup Using TAR

This playbook creates files, compresses them into a backup using the `tar` command, and copies the backup locally.

### Tasks:
1. **Create Files**
   - Creates a list of files with dummy content.
2. **Create a Backup Using tar**
   - Compresses the created files into a backup using the `tar` command.
3. **Verify Backup Exists**
   - Uses the `stat` module to check if the backup file exists.
4. **Copy the Backup Locally**
   - Copies the backup to a local destination if it exists.

## Playbook 7: Configure a Cron Job to Backup Files Locally

This playbook sets up a cron job to back up a specified directory to a local backup directory every night at midnight.

### Tasks:
1. **Ensure the Backup Directory Exists**
   - Creates the backup directory if it doesn’t already exist. This ensures that there’s a dedicated space for storing backup archives.
   
2. **Create the Cron Job**
   - Sets up a cron job to run at midnight. The cron job will create a `.tar.gz` archive of the specified directory and store it in the backup directory.
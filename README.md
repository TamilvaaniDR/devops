# Docker + NGINX Web Application – Day 3

## Objective
To verify Docker installation, create a simple HTML webpage, build a Docker image using NGINX, run the container, resolve port conflicts, and manage containers on an Ubuntu virtual machine.

## Step 1: Check Running Containers
Command:
docker ps

This command shows all currently running Docker containers.

## Step 2: Verify Docker Installation
Command:
docker run hello-world

Explanation:
The Docker client contacts the Docker daemon. The daemon pulls the hello-world image from Docker Hub if not already available. It creates and runs a container, and displays a confirmation message showing Docker is working correctly.

## Step 3: Create Project Directory
Commands:
mkdir nginx-html-demo
cd nginx-html-demo

This creates a new folder for the Docker project and moves into it.

## Step 4: Create HTML File
Command:
nano index.html

This file contains a styled HTML webpage that will be served by NGINX inside the Docker container.

## Step 5: Create Dockerfile
Command:
nano Dockerfile

Dockerfile content:
FROM nginx:latest
COPY index.html /usr/share/nginx/html/index.html

Explanation:
FROM nginx:latest pulls the official NGINX image.
COPY command copies index.html into the default NGINX web directory inside the container.

## Step 6: Build Docker Image
Command:
docker build -t my-nginx-html .

Explanation:
docker build creates a Docker image using the Dockerfile.
-t assigns the name my-nginx-html to the image.
. specifies the current directory as build context.

## Step 7: Run Docker Container
Command:
docker run -d -p 8080:80 my-nginx-html

Explanation:
-d runs the container in background mode.
-p 8080:80 maps port 8080 of the host machine to port 80 inside the container.

## Step 8: Find Server IP Address
Command:
ip a

This displays the system’s IP address.
The application can be accessed in browser using:
http://<server-ip>:8080

## Step 9: Rebuild Image After Editing HTML
Command:
docker build -t my-nginx-html .

This rebuilds the Docker image after making changes to index.html.

## Step 10: Port Already Allocated Error
Error:
Bind for 0.0.0.0:8080 failed: port is already allocated

Reason:
Port 8080 is already being used by another running container.

Solution 1:
docker stop <container_id>
docker rm <container_id>

Solution 2:
docker run -d -p 8081:80 my-nginx-html

This runs the container on a different port.

## Stop All Running Containers
Command:
docker stop $(docker ps -q)

Stops all currently running containers.

## Remove All Containers
Command:
docker rm $(docker ps -aq)

Removes all containers (running and stopped).

## Conclusion
This project demonstrates how Docker containerizes an application using NGINX, how images are built, containers are executed with port mapping, conflicts are handled, and containers are managed effectively in a Linux environment.


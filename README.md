# Day 4 – Jenkins CI/CD Pipeline

## Objective
Create a Jenkins pipeline to automate Docker build and deployment.

## Tools Used
- Jenkins
- Docker
- GitHub
- Ubuntu VM
- NGINX

## Pipeline Stages

1. Clone Repository from GitHub
2. Build Docker Image
3. Run Docker Container
4. Expose Application on Port 8081

## Docker Details

- Image Name: day3-image
- Container Name: day3-container
- Port Mapping: 8081 → 80

## Output

The NGINX web app is successfully deployed inside Docker and accessed via:

http://<VM-IP>:8081

## Author

DevOps Learning – Day 4


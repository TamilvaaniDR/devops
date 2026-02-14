# 🚀 DevOps Complete README
## One-File Documentation (Basics → Industry Level)

---

## 📌 Overview

This README documents my DevOps learning and serves as a long-term reference for real-world and industry-level usage.

Tools covered:
Git, Linux, Docker, Jenkins, AWS, Terraform, Ansible, Kubernetes, Nginx

---

## 1. Git – Version Control System

Git is a distributed version control system used to track source code changes and collaborate with teams.

Why Git is used:
- Track and manage code history
- Enable collaboration
- Support branching and merging
- Integrate with CI/CD pipelines

## 🧠 Git Commands with Clear Explanations (Real-World Use)

git init  
→ Initializes a new Git repository in the current folder.

git clone <repo_url>  
→ Copies a remote repository to your local system.

git status  
→ Shows the current state of files (modified, staged, untracked).

git add .  
→ Stages all modified and new files for commit.

git add <file_name>  
→ Stages a specific file.

git commit -m "message"  
→ Saves staged changes with a meaningful message.

git log  
→ Displays complete commit history.

git log --oneline  
→ Shows commit history in a short, readable format.

git branch  
→ Lists all branches in the repository.

git branch <branch_name>  
→ Creates a new branch.

git checkout <branch_name>  
→ Switches to an existing branch.

git checkout -b <branch_name>  
→ Creates and switches to a new branch.

git branch -d <branch_name>  
→ Deletes a branch after merging.

git pull  
→ Fetches and merges latest changes from remote.

git pull origin main  
→ Updates local main branch from remote.

git fetch  
→ Downloads changes from remote without merging.

git push  
→ Uploads local commits to remote repository.

git push origin main  
→ Pushes commits to the main branch.

git push origin <branch_name>  
→ Pushes a specific branch to remote.

git merge <branch_name>  
→ Merges the specified branch into the current branch.

git merge main  
→ Brings main branch changes into current branch.

git merge --abort  
→ Cancels an ongoing merge if conflicts occur.

git remote -v  
→ Shows connected remote repositories.

git remote add origin <repo_url>  
→ Connects local repository to remote repository.

git reset --soft HEAD~1  
→ Undo last commit but keep changes staged.

git reset --hard HEAD~1  
→ Completely removes last commit and changes.

git stash  
→ Temporarily saves uncommitted changes.

git stash list  
→ Shows all stashed changes.

git stash apply  
→ Restores the most recent stashed changes.

git diff  
→ Shows differences between working directory and staging area.

git diff --staged  
→ Shows differences between staged files and last commit.

git revert <commit_id>  
→ Creates a new commit that reverses a previous commit.

git tag  
→ Lists all tags.

git tag <tag_name>  
→ Creates a version tag for a release.

git config --global user.name "Your Name"  
→ Sets global Git username.

git config --global user.email "your@email.com"  
→ Sets global Git email.


Industry Usage:
- Feature branch workflow
- Pull requests and code reviews
- CI/CD automation

---

## 2. Linux – Server Operating System

Linux is an open-source operating system used in most production servers and cloud environments.

Why Linux is used:
- Stable and secure
- Lightweight
- Powerful command-line interface
- Industry standard for servers

Basic Linux Commands:

ls – List files  
pwd – Current directory  
cd folder – Change directory  
mkdir folder – Create directory  
rm -rf folder – Delete directory  
cp file1 file2 – Copy file  
mv file1 file2 – Move/Rename file  
cat file.txt – View file  
top – Monitor processes  
chmod 755 file.sh – Change permissions  

Industry Usage:
- Server management
- Application deployment
- Log monitoring
- Automation scripting

---

## 3. Docker – Containerization Platform

Docker packages applications and dependencies into containers to ensure consistency across environments.

Why Docker is used:
- Eliminates environment issues
- Faster deployments
- Lightweight compared to VMs
- Easy scalability

Core Concepts:
Image – Application blueprint  
Container – Running instance of image  
Dockerfile – Image build instructions  

Basic Docker Commands:

docker --version  
docker build -t app-name .  
docker images  
docker run -d -p 80:80 app-name  
docker ps  
docker stop <container_id>  
docker rm <container_id>  
docker rmi <image_id>  

Industry Usage:
- Microservices architecture
- CI/CD pipelines
- Kubernetes deployments
- Cloud-native applications

---

## 4. Jenkins – CI/CD Automation Tool

Jenkins is an automation server used for Continuous Integration and Continuous Delivery.

Why Jenkins is used:
- Automates build and deployment
- Reduces manual errors
- Integrates with Git, Docker, AWS

Pipeline Stages:
- Code checkout
- Build
- Test
- Deploy

Industry Usage:
- Automated testing
- Docker image builds
- Continuous deployment

---

## 5. AWS – Cloud Computing Platform

AWS provides on-demand cloud services such as compute, storage, networking, and databases.

Why AWS is used:
- Pay-as-you-go
- Highly scalable
- Global infrastructure
- Secure and reliable

Core Services:
EC2 – Virtual servers  
S3 – Object storage  
IAM – Access management  
VPC – Networking  
RDS – Managed database  
ELB – Load balancer  

Industry Usage:
- Hosting applications
- Auto-scaling systems
- Disaster recovery
- High availability

---

## 6. Terraform – Infrastructure as Code (IaC)

Terraform is an Infrastructure as Code tool used to automate cloud infrastructure provisioning.

Why Terraform is used:
- Infrastructure automation
- Version-controlled infrastructure
- Repeatable deployments
- Multi-cloud support

Terraform Workflow:

terraform init  
terraform plan  
terraform apply  
terraform destroy  

Industry Usage:
- Automated AWS provisioning
- CI/CD infrastructure
- Production environment setup

---

## 7. Ansible – Configuration Management Tool

Ansible is a configuration management and automation tool used to configure servers and deploy applications.

Why Ansible is used:
- Agentless (SSH-based)
- Simple YAML syntax
- Automates repetitive tasks
- Configuration consistency

Core Concepts:
Inventory – List of servers  
Playbook – Automation instructions  
Role – Reusable configurations  

Basic Ansible Commands:

ansible --version  
ansible all -m ping  
ansible-playbook playbook.yml  

Industry Usage:
- Server configuration
- Application deployment
- Patch management
- Infrastructure automation

---

## 8. Kubernetes – Container Orchestration Platform

Kubernetes is used to manage, scale, and deploy containerized applications.

Why Kubernetes is used:
- Container orchestration at scale
- Auto-healing
- Auto-scaling
- High availability

Core Concepts:
Pod – Smallest deployable unit  
Node – Worker machine  
Cluster – Group of nodes  
Service – Application exposure  
Deployment – Manages pods  

Basic Kubernetes Commands:

kubectl get nodes  
kubectl get pods  
kubectl apply -f app.yaml  
kubectl describe pod pod-name  
kubectl delete pod pod-name  

Industry Usage:
- Microservices management
- Production container orchestration
- Cloud-native applications

---

## 9. Nginx – Web Server & Reverse Proxy

Nginx is a high-performance web server and reverse proxy.

Why Nginx is used:
- Handles high traffic
- Acts as reverse proxy
- Load balancing
- SSL termination

Industry Usage:
- Serve static content
- Reverse proxy for backend apps
- Load balancer
- API gateway

---

## 🔄 End-to-End DevOps Flow

Developer → Git Commit → Jenkins CI Pipeline → Docker Build → Kubernetes Orchestration → Nginx Routing → Terraform Infrastructure → AWS Cloud → Production Users


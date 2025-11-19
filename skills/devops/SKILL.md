---
name: devops-infrastructure
description: Manage infrastructure, automate deployments, containerize applications, and ensure system reliability. Use when working with deployment, cloud infrastructure, CI/CD, Docker, Kubernetes, or system operations.
---

# DevOps & Infrastructure

## Quick Start

DevOps combines development and operations to deliver reliable software. Start with the essentials:

### Docker Containerization

```dockerfile
# Dockerfile
FROM python:3.10-slim

WORKDIR /app

# Copy requirements
COPY requirements.txt .
RUN pip install -r requirements.txt

# Copy application
COPY . .

# Expose port
EXPOSE 5000

# Run application
CMD ["python", "app.py"]
```

```bash
# Build and run Docker container
docker build -t myapp:1.0 .
docker run -p 5000:5000 myapp:1.0
```

### Linux Basics

```bash
# Essential commands
ls -la              # List files with details
cd /path/to/dir    # Change directory
mkdir newdir       # Create directory
cp file1 file2     # Copy file
mv file1 file2     # Move/rename file
rm file            # Remove file
cat filename       # Display file contents
grep "pattern" file # Search in file
```

### Git Version Control

```bash
# Initialize and commit
git init
git add .
git commit -m "Initial commit"

# Branching and merging
git branch feature-x
git checkout feature-x
git merge feature-x

# Push to remote
git push origin main
```

## CI/CD Pipeline

```yaml
# GitHub Actions example
name: Deploy
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Build Docker image
        run: docker build -t myapp:${{ github.sha }} .
      - name: Push to registry
        run: docker push myapp:${{ github.sha }}
```

## Kubernetes Basics

```yaml
# Kubernetes deployment
apiVersion: apps/v1
kind: Deployment
metadata:
  name: myapp
spec:
  replicas: 3
  selector:
    matchLabels:
      app: myapp
  template:
    metadata:
      labels:
        app: myapp
    spec:
      containers:
      - name: myapp
        image: myapp:1.0
        ports:
        - containerPort: 5000
```

## Infrastructure as Code

```hcl
# Terraform example - AWS
provider "aws" {
  region = "us-east-1"
}

resource "aws_instance" "web_server" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"

  tags = {
    Name = "web-server"
  }
}
```

## Key Concepts

- **Containerization**: Package apps with dependencies (Docker)
- **Orchestration**: Manage containers at scale (Kubernetes)
- **CI/CD**: Automate testing and deployment
- **Infrastructure as Code**: Define infrastructure in code
- **Monitoring**: Track application and system health

## Learning Path

1. Master Linux command line
2. Learn Docker and containerization
3. Study CI/CD concepts and tools
4. Understand Kubernetes basics
5. Learn Infrastructure as Code (Terraform)
6. Implement monitoring and logging

## Resources

- **Docker Docs**: docs.docker.com
- **Kubernetes Docs**: kubernetes.io/docs
- **Terraform Docs**: terraform.io/docs
- **Linux Academy**: Linux fundamentals

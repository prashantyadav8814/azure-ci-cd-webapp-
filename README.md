# Azure CI/CD Pipeline for Flask Web App

## Overview
This project demonstrates a complete CI/CD pipeline using Azure services.  
Every code push triggers automated build, test, containerization, and deployment.

## Architecture
GitHub → GitHub Actions → Azure Container Registry → Azure App Service

## Tech Stack
- Flask (Python)
- Docker
- GitHub Actions
- Azure Container Registry (ACR)
- Azure App Service

## CI/CD Workflow
1. Code pushed to GitHub
2. GitHub Actions runs unit tests
3. Docker image is built and pushed to ACR
4. Azure App Service pulls the latest image

## How to Run Locally
```bash
docker build -t flaskapp .
docker run -p 5000:5000 flaskapp

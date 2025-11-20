🚀 GitHub Actions Workflow – Run Docker Image from Docker Hub
 
This repository demonstrates how to create a simple GitHub Actions workflow that pulls and runs a Docker image from Docker Hub using a GitHub-hosted runner
## The workflow is useful for:
>> Testing Docker images
>> Running containerized apps inside CI
>> Automating deployments and validation

## What This Workflow Does
✔ Pulls code from repository
✔ Logs in to Docker Hub (optional)
✔ Pulls a Docker image from Docker Hub
✔ Runs the image inside GitHub Runner
✔ Verifies the container using docker ps

## Using Private Docker Hub Images
If your image is private, add the following secrets in GitHub:
Go to Repository → Settings → Secrets → Actions
Add:
DOCKERHUB_USERNAME
DOCKERHUB_TOKEN (from Docker Hub → Access Tokens)

The workflow will authenticate before pulling the image.

**Workflow Execution Flow**

Developer Push → GitHub Repo
        |
        ↓
GitHub Actions Trigger
        |
        ↓
Ubuntu GitHub-Hosted Runner
        |
------------------------------------------------
| Checkout repo                                 |
| Login to Docker Hub (optional)                |
| Pull image from Docker Hub                    |
| Run Docker container                          |
| Show container status                         |
------------------------------------------------

**Summary**
With this GitHub Actions workflow, you can easily:
Pull Docker images from Docker Hub
Run containers inside GitHub CI
Automate testing, verification & deployment
Work with both public and private images

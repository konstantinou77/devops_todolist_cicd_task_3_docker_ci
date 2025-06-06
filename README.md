# GitHub Actions Workflow with Docker Build & Push to DockerHub

# Project Overview:

This project extends the existing GitHub Actions CI workflow by adding automation
to build and push Docker images to DockerHub. The workflow enhances continuous
integration by packaging the application into a Docker container and securely
uploading it to a DockerHub repository, enabling easier deployment and distribution.

# Tech Stack:

- GitHub Actions (CI/CD)
- Docker
- DockerHub Registry
- GitHub Repository Secrets for credentials management

# What was done:

- Added a new docker-ci job to the GitHub Actions workflow.
- Docker images are tagged with the current commit hash for traceability.
- DockerHub credentials are securely stored and accessed via GitHub Repository Secrets.
- The docker-ci job runs only on the main branch to ensure production readiness.
- Uploading artifacts from the previous job is restricted to runs on the main branch.
- Steps in the docker-ci job include:
  - Logging into DockerHub Registry.
  - Building the Docker image using the provided Dockerfile.
  - Pushing the tagged Docker image to the DockerHub Registry.


# Link to the successful GitHub Actions run:
https://github.com/konstantinou77/devops_todolist_cicd_task_3_docker_ci/actions/runs/14709789862


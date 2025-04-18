# GoLang Docker CI/CD to GitHub Container Registry (GHCR)

This repository demonstrates a complete CI/CD pipeline using **GitHub Actions** to build and push a Docker image of a GoLang project to **GitHub Container Registry (GHCR)**.

## 🚀 Features

- GoLang-based backend service
- Dockerized application
- CI/CD workflow using GitHub Actions
- Push to GHCR automatically on every commit to the main branch

## 🛠️ Tech Stack

- GoLang
- Docker
- GitHub Actions (CI/CD)
- GitHub Container Registry (GHCR)

## 🧪 How It Works

1. GitHub Action workflow is triggered on `push` to the `main` branch.
2. It builds the Docker image.
3. Authenticates with GHCR using `GITHUB_TOKEN`.
4. Pushes the image to GHCR.

## 📂 Docker Image

You can find the Docker image here:  
`ghcr.io/<your-username>/<your-repo-name>:<tag>`

> Replace `<your-username>` and `<your-repo-name>` with your GitHub details.

## ⚠️ Troubleshooting Faced

- **Dockerfile Path Error**: The build was failing due to an incorrect Dockerfile path. Fixed by updating the correct path in the GitHub Actions workflow.
- **403 Forbidden Error**: The GitHub token used for authentication did not have the required `read/write` permissions. Solved by setting proper permissions in **Repository Settings > Actions > Secrets and Variables**.

## ✅ How to Use

1. Clone this repo:
   ```bash
   git clone https://github.com/AqibHafeez473/nodejs-app-CICD-githubaction.git
   cd nodejs-app-CICD-githubaction

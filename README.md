# 🚀 Node Docker Push – CI/CD with GitHub Actions

This project demonstrates a simple **Node.js app** that is **Dockerized** and automatically pushed to **Docker Hub** using **GitHub Actions**.

## 📦 What's Inside

- 🛠️ Node.js app with `index.js`
- 🐳 Dockerfile to build the image
- 🤖 `.github/workflows/docker.yml` GitHub Actions workflow
- 🔐 Uses secrets `DOCKER_USERNAME` and `DOCKER_PASSWORD` for secure login

## ⚙️ GitHub Actions Workflow

Whenever you `push` to `main`, the workflow:

1. Logs in to Docker Hub
2. Builds the Docker image
3. Tags it as `latest`
4. Pushes it to:  
   [📦 Docker Hub Repo](https://hub.docker.com/r/ritesh355/node-docker-push)

## 🚀 Try it Yourself

```bash
git clone git@github.com:ritesh355/node-docker-push.git
cd node-docker-push
docker build -t ritesh355/node-docker-push .
docker run -p 3000:3000 ritesh355/node-docker-push

---
Then open: http://localhost:3000

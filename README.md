#  Next.js DevOps Project

- This project demonstrates how to containerize a Next.js application, push it to GitHub Container Registry (GHCR), and deploy it to Kubernetes (Minikube) using CI/CD automation with GitHub Actions.
---
## Setup Instructions
**Prerequisites**

- Node.js & npm
- Docker
- Minikube & kubectl
- Git
---

## **Quick Start**

Run the project **locally, with Docker, or on Minikube**:

### 1️ Clone the Repository

```bash
git clone https://github.com/tejaswini2704/nextjs-devops.git
cd nextjs-devops
```

### 2️ Run Locally

```bash
npm install
npm run dev

```

### 3️ Build & Run with Docker

```bash
docker build -t nextjs-devops-app .
docker run -p 3000:3000 nextjs-devops-app

```

### 4️ Deploy on Minikube

```bash
minikube start
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
kubectl get pods
minikube service nextjs-service

```

### 5️ Pull GHCR Image

```bash
docker pull ghcr.io/tejaswini2704/nextjs-devops-app:latest
```

---

## **Project Structure**

```
nextjs-devops/
├── .github/workflows/      # GitHub Actions workflow
├── k8s/                    # Kubernetes manifests
│   ├── deployment.yaml
│   └── service.yaml
├── pages/                  # Next.js pages
├── Dockerfile              # Dockerfile for containerization
├── package.json
└── README.md
```

---

## **Project Highlights / What I Did**

* Created a **Next.js starter application**
* Wrote an **optimized Dockerfile** for containerization
* Built **GitHub Actions workflow** to:

  * Build Docker image on push to `main`
  * Push the image to **GHCR** with proper tagging
* Created **Kubernetes manifests** (`deployment.yaml` and `service.yaml`)
* Deployed the app locally using **Minikube**
* Documented **setup instructions, commands, and deployment steps**

---

## **Links**

* Repository: [https://github.com/tejaswini2704/nextjs-devops](https://github.com/tejaswini2704/nextjs-devops)
* Docker Image: [https://ghcr.io/tejaswini2704/nextjs-devops-app](https://ghcr.io/tejaswini2704/nextjs-devops-app)


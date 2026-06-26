# Deploy a Multi-Container Web App on GCP using Terraform & GKE 🚀

This repository demonstrates a fully automated End-to-End DevOps pipeline that builds, ships, and deploys a containerized web application into a production-ready Google Kubernetes Engine (GKE) cluster using Infrastructure as Code (IaC) and GitOps principles.

## 🛠️ Tech Stack & Architecture

* **Docker:** Containers and packages the web application with an Nginx environment.
* **GitHub Actions:** Automates the CI/CD pipeline for building and pushing images securely.
* **Docker Hub:** Acts as the secure container registry for storing versioned images.
* **Terraform:** Manages the Cloud Infrastructure as Code (IaC), provisioning VPCs and GKE clusters.
* **Google Cloud Platform (GCP):** Production cloud provider hosting the infrastructure.
* **Kubernetes (GKE):** Orchestrates the containers, ensuring high availability, self-healing, and auto-scaling.

---

## 🔄 Project Roadmap & Progress

- [x] **Containerization:** Package the web app using Docker & Nginx.
- [x] **CI/CD Pipeline:** Integrate GitHub Actions to securely log in, build, and push versioned images to Docker Hub on every Git push.
- [ ] **Infrastructure as Code (IaC):** Write Terraform manifests to provision a secure VPC and GKE cluster on Google Cloud.
- [ ] **Kubernetes Deployment:** Deploy the application into GKE with automated scaling and a public Load Balancer.

---

## 🚀 How the CI Pipeline Works Currently

Every time a `git push` is triggered on the `main` branch:
1. **GitHub Actions** provisions a clean runner.
2. Secret keys (`DOCKERHUB_USERNAME` and `DOCKERHUB_TOKEN`) are securely injected.
3. The Docker image is built and automatically pushed to the registry: `ahmedelhassan77/docker-cloud-app`.

---

## 🛠️ How to Run Locally

To pull and run the current stable container image from Docker Hub locally:

```bash
docker pull ahmedelhassan77/docker-cloud-app:latest
docker run -d -p 8080:80 ahmedelhassan77/docker-cloud-app:latest
## Implemented By
Ahmed El-Hassan - Cloud Engineer

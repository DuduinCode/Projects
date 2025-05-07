# 🚀 GitOps Workflow using ArgoCD on Kubernetes (AWS EC2)

This project demonstrates how to implement a GitOps workflow using **ArgoCD** on a **Kubernetes cluster** hosted on an **AWS EC2 instance**. It deploys a sample application (guestbook) by syncing a GitHub repository to the cluster using ArgoCD.

---

## 📌 Project Overview

**GitOps** is a modern DevOps practice that uses Git as the single source of truth for infrastructure and application code. **ArgoCD** is a declarative GitOps continuous delivery tool for Kubernetes.

In this project, we:
- Set up Kubernetes using Minikube on AWS EC2
- Installed and configured ArgoCD
- Deployed a sample app from a GitHub repo
- Managed the deployment using GitOps principles

---

## 🛠️ Tech Stack

| Tool           | Purpose                            |
|----------------|------------------------------------|
| AWS EC2        | Hosting the Kubernetes Cluster     |
| Ubuntu 22.04   | Operating System on EC2            |
| Minikube       | Local Kubernetes Cluster           |
| kubectl        | CLI to interact with Kubernetes    |
| ArgoCD         | GitOps Continuous Delivery         |
| GitHub         | App Manifests Repository           |

---

## ⚙️ Setup Instructions

### 1. 🚀 Launch AWS EC2 Instance

- Instance type: `t2.medium` recommended
- OS: Ubuntu 22.04
- Open ports: `22`, `80`, `30000–32767` in security group

### 2. 🔧 Install Minikube and Kubernetes Tools

```bash
sudo apt update
sudo apt install -y curl wget apt-transport-https ca-certificates gnupg lsb-release docker.io
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
minikube start --driver=docker

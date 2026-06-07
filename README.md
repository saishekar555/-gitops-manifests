# 🚀 GitOps & DevSecOps on Azure Kubernetes Service (AKS)

## 📌 Project Overview

This project demonstrates a complete GitOps and DevSecOps implementation using Azure Kubernetes Service (AKS), ArgoCD, GitHub, Kubernetes, Gitleaks, and Trivy.

The application deployment is fully automated through GitOps principles, where Kubernetes manifests stored in GitHub serve as the single source of truth. ArgoCD continuously monitors the repository and automatically synchronizes changes to the AKS cluster.

Security is integrated throughout the deployment lifecycle using Gitleaks for secret detection and Trivy for Kubernetes manifest and container image vulnerability scanning.

---

# 🏗️ Architecture

```text
Developer
    │
    ▼
GitHub Repository
    │
    ▼
Gitleaks Secret Scan
    │
    ▼
Trivy Config Scan
    │
    ▼
Docker Image Scan
    │
    ▼
ArgoCD
    │
    ▼
Azure Kubernetes Service (AKS)
```

---

# 🛠️ Technologies Used

* Microsoft Azure
* Azure Kubernetes Service (AKS)
* Kubernetes
* ArgoCD
* GitHub
* Docker
* Azure Container Registry (ACR)
* Gitleaks
* Trivy
* Azure CLI
* Kubectl
* YAML

---

# ✨ Features

## GitOps

* Declarative Kubernetes deployments
* Git as Single Source of Truth
* Automatic synchronization using ArgoCD
* Continuous deployment to AKS
* Self-healing cluster state

## DevSecOps

### Gitleaks

Secret scanning before deployment.

Detects:

* Passwords
* API Keys
* Access Tokens
* Credentials

### Trivy Configuration Scanning

Kubernetes manifest security validation.

Detects:

* Privileged containers
* Missing security contexts
* Running as root
* Missing resource limits
* Namespace security issues

### Trivy Image Scanning

Container image vulnerability scanning.

Detects:

* Critical CVEs
* High Severity CVEs
* Medium Severity CVEs
* Low Severity CVEs

---

# ☸️ Kubernetes Resources

## Deployment

* NGINX Application Deployment
* Replica Scaling
* Resource Requests & Limits
* Security Policies

## Service

* LoadBalancer Service
* External Access Configuration

## ArgoCD Application

* GitHub Integration
* Automatic Sync
* Drift Detection
* Self-Healing

---

# 🚀 Deployment Steps

## Clone Repository

```bash
git clone https://github.com/saishekar555/-gitops-manifests.git
```

## Deploy ArgoCD Application

```bash
kubectl apply -f argocd-app.yaml
```

## Verify Resources

```bash
kubectl get pods
kubectl get svc
kubectl get deployments
```

## Verify ArgoCD

```bash
kubectl get applications -n argocd
```

---

# 🔐 DevSecOps Validation

## Secret Scanning

```bash
gitleaks detect --source .
```

## Kubernetes Security Scan

```bash
trivy config deployment.yaml
```

## Container Vulnerability Scan

```bash
trivy image nginx:latest
```

---

# 🔄 GitOps Demonstration

Example:

Update replicas in deployment.yaml

```yaml
replicas: 5
```

Push changes:

```bash
git add .
git commit -m "Scale nginx deployment"
git push
```

ArgoCD automatically detects the change and synchronizes the AKS cluster.

---

# 📊 Project Outcomes

Through this project I gained hands-on experience in:

* GitOps Implementation
* DevSecOps Practices
* Azure Kubernetes Service (AKS)
* Kubernetes Administration
* ArgoCD Continuous Deployment
* Vulnerability Management
* Infrastructure Security
* Container Security
* CI/CD Concepts

---

# 🎯 Interview Highlights

This project demonstrates:

✅ GitOps using ArgoCD

✅ AKS Deployment Automation

✅ Kubernetes Management

✅ Gitleaks Secret Scanning

✅ Trivy Manifest Scanning

✅ Trivy Image Vulnerability Scanning

✅ Self-Healing Deployments

✅ Azure Cloud Operations

---

# 👨‍💻 Author

Dammoju Sai Shekar Chary

Azure DevOps Engineer | Azure Administrator

GitHub:
https://github.com/saishekar555

LinkedIn:
https://linkedin.com/in/saishekar555

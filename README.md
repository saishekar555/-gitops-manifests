# GitOps DevSecOps Project on Azure Kubernetes Service (AKS)

## Project Overview

This project demonstrates an end-to-end GitOps and DevSecOps implementation using Kubernetes, Azure Kubernetes Service (AKS), ArgoCD, Gitleaks, Trivy, Docker, and GitHub.

The objective of this project is to automate application deployment while integrating security scanning throughout the software delivery lifecycle.

---

## Architecture

GitHub Repository
↓
Gitleaks Secret Scan
↓
Trivy Configuration Scan
↓
Docker Image Build
↓
Trivy Image Vulnerability Scan
↓
Azure Container Registry (ACR)
↓
ArgoCD GitOps Sync
↓
Azure Kubernetes Service (AKS)

---

## Technologies Used

* Azure Kubernetes Service (AKS)
* Kubernetes
* ArgoCD
* GitHub
* Docker
* Azure Container Registry (ACR)
* Gitleaks
* Trivy
* GitOps
* DevSecOps
* YAML
* Azure CLI
* Kubectl

---

## Project Features

### GitOps Deployment

* Declarative Kubernetes manifests stored in GitHub
* Automatic synchronization using ArgoCD
* Continuous deployment through GitOps workflow

### DevSecOps Security Integration

#### Gitleaks

Used for secret detection in source code repositories.

Example:

gitleaks detect --source .

Detects:

* API Keys
* Tokens
* Passwords
* Secrets

#### Trivy Configuration Scan

Used to scan Kubernetes manifests for security misconfigurations.

Example:

trivy config deployment.yaml

Checks:

* Privileged Containers
* Missing Resource Limits
* Security Context Issues
* Root User Execution

#### Trivy Image Scan

Used to scan Docker images for vulnerabilities.

Example:

trivy image nginx:latest

Detects:

* Critical Vulnerabilities
* High Vulnerabilities
* Medium Vulnerabilities
* Low Vulnerabilities

---

## Kubernetes Resources

### Deployment

* NGINX Deployment
* Multiple Replica Pods
* Resource Requests and Limits
* Security Context Configuration

### Service

* Kubernetes Service
* Cluster Networking
* Load Balancer Exposure

### ArgoCD Application

* Git Repository Integration
* Automatic Sync
* Self-Healing
* Continuous Reconciliation

---

## Deployment Steps

### Clone Repository

git clone https://github.com/saishekar555/gitops-devsecops-project.git

### Apply ArgoCD Application

kubectl apply -f argocd-app.yaml

### Verify Deployment

kubectl get pods

kubectl get deployments

kubectl get svc

### Access ArgoCD

kubectl get svc -n argocd

---

## Security Validation

Run Secret Scan:

gitleaks detect --source .

Run Kubernetes Manifest Scan:

trivy config deployment.yaml

Run Container Image Scan:

trivy image nginx:latest

---

## Monitoring GitOps Changes

Update deployment.yaml:

replicas: 5

Commit and Push:

git add .

git commit -m "Scale application"

git push

ArgoCD automatically detects changes and synchronizes AKS cluster state with GitHub repository.

---

## Learning Outcomes

Through this project I gained hands-on experience in:

* GitOps Deployment Strategy
* Kubernetes Administration
* Azure Kubernetes Service (AKS)
* ArgoCD Automation
* DevSecOps Practices
* Container Security
* Vulnerability Management
* Infrastructure Security Validation
* Continuous Deployment

---

## Author

Dammoju Sai Shekar Chary

Azure DevOps Engineer

GitHub:
https://github.com/saishekar555

LinkedIn:
https://linkedin.com/in/saishekar555

# GitOps Kubernetes Manifests

Kubernetes manifests for the GitOps Node.js application.

## Structure
```
base/
├── namespace.yaml   # Application namespace
├── deployment.yaml  # Application deployment
└── service.yaml     # Application service
```

## Deployment
This repository is monitored by ArgoCD for automatic deployment.

## Manual Deployment (for testing)
```bash
kubectl apply -f base/
```

## Access Application
```bash
# Get service URL (Minikube)
minikube service gitops-service -n gitops-app

# Or port-forward
kubectl port-forward -n gitops-app svc/gitops-service 8080:80
```

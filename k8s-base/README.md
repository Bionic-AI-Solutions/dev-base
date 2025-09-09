# K8s-Base Setup

This is a minimal Kubernetes pod setup with SSH access only.

## Features
- SSH access via NodePort service
- Minimal container with development tools
- No database or application services
- Direct pod access for development

## Usage

### Deploy to Kubernetes
```bash
kubectl apply -f k8s-base/manifests/
```

### SSH Access
```bash
# Get the NodePort
kubectl get svc <project-name>-ssh

# SSH to the pod
ssh developer@<node-ip> -p <nodeport>
# Password: dev123
```

### Cleanup
```bash
kubectl delete -f k8s-base/manifests/
```

# Kubernetes Zero to Hero Learning Path

![Diagram](kubernetes-architecture.PNG)

## Preparation on Your Laptop: Step-by-Step Guide

### 1. Docker Desktop Installation
Follow the [official guide](https://www.docker.com/products/docker-desktop/) to install Docker Desktop on your system.

### 2. WSL Installation on Windows
Set up Windows Subsystem for Linux (WSL) by following the [Microsoft WSL documentation](https://learn.microsoft.com/en-us/windows/wsl/install).

### 3. Kind Installation on Windows and WSL
#### Kind Installation on Linux
Use the following commands based on your system architecture:

```bash
# For AMD64 / x86_64
[ $(uname -m) = x86_64 ] && curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.26.0/kind-linux-amd64

# For ARM64
[ $(uname -m) = aarch64 ] && curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.26.0/kind-linux-arm64

# Make it executable
chmod +x ./kind

# Move it to a directory in your PATH
sudo mv ./kind /usr/local/bin/kind
Kind Installation on Windows
```

### 4. Kind Installation on Windows

### For Windows, run the following commands in PowerShell:

```
curl.exe -Lo kind-windows-amd64.exe https://kind.sigs.k8s.io/dl/v0.26.0/kind-windows-amd64
Move-Item .\kind-windows-amd64.exe c:\some-dir-in-your-PATH\kind.exe
```
4. Creating a Cluster and Configuring Nodes
Using PowerShell Command Line

 Create a Kubernetes cluster with Kind:
 ```
  kind create cluster
```
Label worker nodes:
 ```

kubectl label nodes kind-worker node-role.kubernetes.io/worker=
kubectl label nodes kind-worker2 node-role.kubernetes.io/worker=
kubectl get nodes
```






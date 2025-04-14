# 09. Kubernetes

## Homework Assignment 0: Finish full install k8s

## Homework Assignment 1: KinD Kubernetes Cluster Setup
1. Install kubectl on Linux
```
debian@vbox ~/it-academy-training (master)> kubectl version --client
Client Version: v1.32.3
Kustomize Version: v5.5.0
```
2. Install Kind
```
debian@vbox ~/it-academy-training (master)> kind --version
kind version 0.27.0
```  
3. Create kind cluster.
```
debian@vbox ~/it-academy-training (master)> kind create cluster
Creating cluster "kind" ...
 ✓ Ensuring node image (kindest/node:v1.32.2) 🖼 
 ✓ Preparing nodes 📦  
 ✓ Writing configuration 📜 
 ✓ Starting control-plane 🕹️ 
 ✓ Installing CNI 🔌 
 ✓ Installing StorageClass 💾 
Set kubectl context to "kind-kind"
You can now use your cluster with:

kubectl cluster-info --context kind-kind

Thanks for using kind! 😊
```
4. Verify cluster via ```kubectl```

```
debian@vbox ~/it-academy-training (master)> kubectl cluster-info
Kubernetes control plane is running at https://127.0.0.1:35677
CoreDNS is running at https://127.0.0.1:35677/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy
```
## Homework Assignment 2: Minikube Kubernetes Cluster Setup

## Homework Assignment 3: GitHub Actions for KinD Cluster Setup

## Homework Assignment 4: GitHub Actions for Minikube Cluster Setup

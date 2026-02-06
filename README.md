# Kubernetes (K8s) Practice – KIND 🚀

This repository is created for **practicing Kubernetes using KIND (Kubernetes in Docker)**.  
All YAML files are for **learning and reference purposes only**.

🎯 Purpose
Practice Kubernetes fundamentals
Learn KIND cluster setup
Quick kubectl reference
DevOps interview preparation

👤 Author: Yashraj Gohil
⭐ This is a practice repository

## 📂 Files
<img width="300" height="200" alt="image" src="https://github.com/user-attachments/assets/ec74a7ec-b6a5-4ac1-8400-0a652672926f" />


## 🔧 Create KIND Cluster
```bash

kind create cluster --name nginx-cluster --config config.yml
kubectl get nodes

📦 Create Namespace
kubectl apply -f namespace.yml
kubectl get ns

🚀 Apply Resources (Namespace: nginx)
kubectl apply -f pod.yml -n nginx
kubectl apply -f deployment.yml -n nginx
kubectl apply -f service.yml -n nginx
kubectl apply -f job.yml -n nginx

🔍 Verify Resources
kubectl get pods -n nginx
kubectl get deployments -n nginx
kubectl get svc -n nginx
kubectl get jobs -n nginx

📜 View Logs
kubectl logs <pod-name> -n nginx
kubectl logs job/<job-name> -n nginx

🧪 Describe (Debug)
kubectl describe pod <pod-name> -n nginx
kubectl describe deployment <deployment-name> -n nginx
kubectl describe service <service-name> -n nginx

❌ Delete Resources
kubectl delete -f pod.yml -n nginx
kubectl delete -f deployment.yml -n nginx
kubectl delete -f service.yml -n nginx
kubectl delete -f job.yml -n nginx
kubectl delete -f namespace.yml

Delete everything:
kubectl delete -f .

🧹 Delete KIND Cluster
kind delete cluster --name nginx-cluster


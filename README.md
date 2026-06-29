# 🚀 Kubernetes Enterprise Cluster on VMware Cloud Director

A production-style multi-node Kubernetes cluster deployed on VMware Cloud Director using **Kubernetes**, **kubeadm**, and **containerd**.

---

## 📌 Project Overview

This project demonstrates the deployment and management of an enterprise Kubernetes cluster consisting of one control plane node and four worker nodes.

The cluster hosts multiple applications and services, demonstrating:

- Multi-node Kubernetes architecture
- Namespace isolation
- Persistent storage
- Resource management
- Object storage
- Monitoring and administration
- Dashboard-based cluster management

---

# 🏗️ Architecture

```text
                           Internet
                               │
                        Public IP Access
                               │
                     Kubernetes Dashboard
                               │
                     ┌─────────────────┐
                     │   k8s-master    │
                     │  Control Plane  │
                     └────────┬────────┘
                              │
        ┌─────────────────────┼─────────────────────┐
        │                     │                     │
        │                     │                     │
┌─────────────┐     ┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│  worker-1   │     │  worker-2   │     │  worker-3   │     │  worker-4   │
│  Web Node   │     │ Database    │     │ Cache Node  │     │ Storage     │
└──────┬──────┘     └──────┬──────┘     └──────┬──────┘     └──────┬──────┘
       │                   │                   │                   │
   ┌───▼───┐         ┌─────▼─────┐        ┌────▼────┐        ┌─────▼─────┐
   │ Nginx │         │   MySQL   │        │  Redis  │        │   MinIO   │
   └───────┘         ├───────────┤        └─────────┘        └───────────┘
                     │PostgreSQL │
                     └───────────┘
```

---

# 🖥️ Infrastructure

| Node | Role | IP Address |
|------|------|------------|
| k8s-master | Control Plane | 192.168.0.2 |
| worker-1 | Web Services | 192.168.0.3 |
| worker-2 | Database Services | 192.168.0.4 |
| worker-3 | Cache Services | 192.168.0.5 |
| worker-4 | Storage Services | 192.168.0.6 |

---

# ⚙️ Technologies Used

- Kubernetes
- kubeadm
- containerd
- Calico CNI
- VMware Cloud Director
- Nginx
- Apache
- MySQL
- PostgreSQL
- Redis
- MinIO
- Metrics Server
- Kubernetes Dashboard
- Git
- GitHub

---

# 📂 Repository Structure

```text
Kubernetes-Enterprise-Cluster/
│
├── configs/
│   ├── nodes.txt
│   ├── node-usage.txt
│   ├── pods.txt
│   ├── services.txt
│   └── website-configmap.yaml
│
├── manifests/
│   ├── apache-deployment.yaml
│   ├── minio-deployment.yaml
│   ├── minio-service.yaml
│   ├── mysql-deployment.yaml
│   ├── mysql-pvc.yaml
│   ├── nginx-deployment.yaml
│   ├── nginx-service.yaml
│   ├── postgres-deployment.yaml
│   └── redis-deployment.yaml
│
├── screenshots.pdf
├── documentation.pdf
│
├── README.md
├── SETUP-GUIDE.md
├── LICENSE
└── .gitignore
```

---

# 🚀 Cluster Features

✅ Multi-node Kubernetes Cluster

✅ Namespace Isolation

✅ Workload Scheduling

✅ Persistent Storage

✅ ConfigMaps

✅ Resource Management

✅ Rolling Updates

✅ Rollback Functionality

✅ Self-Healing Deployments

✅ Application Scaling

✅ Resource Monitoring

✅ Kubernetes Dashboard

✅ Object Storage

---

# 📦 Deployed Applications

| Application | Namespace | Purpose |
|------------|-----------|---------|
| Nginx | web | Web Server |
| Apache | web | Web Server |
| MySQL | database | Relational Database |
| PostgreSQL | database | Relational Database |
| Redis | cache | In-Memory Cache |
| MinIO | storage | Object Storage |

---

# 📊 Monitoring

The cluster includes:

- Metrics Server
- Node Resource Monitoring
- Pod Resource Monitoring
- Kubernetes Dashboard

Commands:

```bash
kubectl top nodes

kubectl top pods -A
```

---

# 🔄 Kubernetes Demonstrations

## Scaling

```bash
kubectl scale deployment nginx --replicas=5 -n web
```

## Self-Healing

```bash
kubectl delete pod POD_NAME -n web
```

## Rolling Updates

```bash
kubectl set image deployment/nginx nginx=nginx:1.27 -n web
```

## Rollback

```bash
kubectl rollout undo deployment nginx -n web
```

---

# 📈 Kubernetes Dashboard

The Kubernetes Dashboard provides:

- Pod Monitoring
- Deployment Monitoring
- Namespace Management
- Service Monitoring
- Resource Usage
- Cluster Administration

---

# 📋 Verification Commands

```bash
kubectl get nodes

kubectl get pods -A

kubectl get svc -A

kubectl get deployments -A

kubectl get pvc -A

kubectl top nodes

kubectl top pods -A
```

---

# 🎯 Learning Outcomes

- Kubernetes Cluster Deployment
- Container Orchestration
- Multi-Node Architecture
- Persistent Storage Management
- Resource Allocation
- Monitoring and Administration
- Application Deployment
- Cluster Management
- Infrastructure as Code

---

# 👨‍💻 Author

**Shivani Sharma**

B.Tech Computer Science Engineering  
Amity University Noida

---

# ⭐ Project Highlights

- 5-Node Kubernetes Cluster
- VMware Cloud Director Deployment
- Enterprise Workload Segregation
- Object Storage Implementation
- Dashboard-Based Management
- Production-Style Architecture
- Real-World Kubernetes Concepts

---

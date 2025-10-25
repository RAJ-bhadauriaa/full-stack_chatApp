**Built by:** Raj Bhadauria  ......
**LinkedIn:** [linkedin.com/in/raj-bhadauria-58924219b](https://www.linkedin.com/in/raj-bhadauria-58924219b/)


# 📦 Full-Stack Chat App – Kubernetes Deployment

This project is a **full-stack real-time chat application** deployed on **Kubernetes** using `kind` on an **Azure Linux VM**.  
The original app (frontend in React + Nginx, backend in Node.js + Express, and MongoDB database) was containerized and fully orchestrated with Kubernetes manifests I created from scratch.

---

## 🚀 Tech Stack

- **Frontend**: React + Nginx (serves the React build)
- **Backend**: Node.js + Express (chat API & WebSocket handling)
- **Database**: MongoDB (persistent data storage)
- **Orchestration**: Kubernetes (`kind` cluster on Azure VM)
- **Containerization**: Docker (images pushed to Docker Hub)
- **Networking**: Kubernetes Services + Ingress
- **Storage**: PersistentVolume & PersistentVolumeClaim for MongoDB data
- **Secrets Management**: Kubernetes Secrets for DB credentials

---

## 📂 Kubernetes Manifests in This Repo

| File | Purpose |
| --- | --- |
| `namespace.yml` | Dedicated namespace for isolation |
| `frontend-deployment.yml` | Deploys React app with Nginx |
| `frontend-service.yml` | Exposes frontend pod to Ingress |
| `backend-deployment.yml` | Deploys Node.js backend |
| `backend-service.yml` | Internal access for backend API |
| `mongodb-deployment.yml` | Deploys MongoDB database |
| `mongodb-pv.yml` | Static PersistentVolume |
| `mongodb-pvc.yml` | PersistentVolumeClaim for MongoDB |
| `mongodb-service.yml` | Internal MongoDB service |
| `ingress.yml` | Public HTTP access on port 80 |
| `secrets.yml` | Stores MongoDB credentials securely |

---

## 🌐 Deployment Overview

1. **Built & pushed Docker images** for frontend and backend to my Docker Hub. : https://hub.docker.com/repositories/rajbhadauriaa
2. **Wrote Kubernetes manifests** for all components (deployments, services, ingress, PV, PVC, secrets).
3. **Applied all manifests** using:
   ```bash
   kubectl apply -f .
4. **Accessed the application** via:
   http://Azure-VM-Public-IP:80


📄 Original Project-
The original project without Kubernetes manifests is preserved in ORIGINAL-README.md.



   🔗 Author-
Raj Bhadauria:
Cloud & DevOps Enthusiast









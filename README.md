# 📚 Library Management System

### Enterprise Application Automation with Kubernetes & Monitoring Stack

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge\&logo=kubernetes\&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge\&logo=docker\&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge\&logo=prometheus\&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge\&logo=grafana\&logoColor=white)
![AWS](https://img.shields.io/badge/AWS_EC2-FF9900?style=for-the-badge\&logo=amazonaws\&logoColor=white)

---

## 🚀 Overview

A web-based **Library Management System** containerized using Docker, orchestrated with Kubernetes, and monitored via Prometheus & Grafana on AWS EC2.

🔗 **Live Demo:** http://librarymanagesystem.netlify.app
🐳 **Docker Hub:** https://hub.docker.com/r/nitin3886/library-app

---

## ✨ Features

### 📌 Application

* Add, view, and delete books
* Separate interfaces for users and librarians
* Responsive UI design
* Client-side data handling (JavaScript-based)

### ⚙️ DevOps & Monitoring

* Docker containerization using `nginx:alpine`
* Kubernetes deployment with 3 replicas
* Self-healing and auto-scaling support
* Prometheus metrics scraping (15s interval)
* Grafana dashboards for system monitoring
* AWS EC2 deployment (Ubuntu)

---

## 📁 Project Structure

```
Library_Management_System/
│
├── index.html
├── styles.css
├── script.js
├── db.js
│
├── librarian/
├── user/
│
├── Dockerfile
└── k8s/
    ├── deployment.yaml
    ├── service.yaml
    ├── prometheus.yaml
    ├── grafana.yaml
    └── node-exporter.yaml
```

---

## 🛠️ Tech Stack

| Layer            | Technology                 |
| ---------------- | -------------------------- |
| Frontend         | HTML, CSS, JavaScript      |
| Containerization | Docker                     |
| Orchestration    | Kubernetes (Minikube)      |
| Monitoring       | Prometheus + Node Exporter |
| Visualization    | Grafana                    |
| Cloud            | AWS EC2                    |

---

## ⚡ Getting Started

### 1️⃣ Run Locally

```bash
git clone https://github.com/Nitin3886/k8s-library-monitoring.git
cd k8s-library-monitoring
```

Open `index.html` in browser.

---

### 2️⃣ Run with Docker

```bash
docker pull nitin3886/library-app:latest
docker run -d -p 8080:80 nitin3886/library-app
```

Access → http://localhost:8080

---

### 3️⃣ Run with Kubernetes

```bash
minikube start
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```

Deploy monitoring:

```bash
kubectl apply -f k8s/node-exporter.yaml
kubectl apply -f k8s/prometheus.yaml
kubectl apply -f k8s/grafana.yaml
```

---

## 🌐 Access Services

| Service    | URL                 |
| ---------- | ------------------- |
| App        | http://YOUR_IP:8080 |
| Prometheus | http://YOUR_IP:9090 |
| Grafana    | http://YOUR_IP:3000 |

---

## 📊 Monitoring Setup (Grafana)

1. Login → `admin / admin123`
2. Add Prometheus datasource
3. Import Dashboard → ID **1860**

---

## 🔄 Kubernetes Self-Healing

```bash
kubectl delete pod <pod-name>
kubectl get pods -w
```

Kubernetes automatically recreates the pod.

---

## 🧠 Architecture

```
User → Browser → Kubernetes Service → Pods
Metrics → Node Exporter → Prometheus → Grafana
```

---

## 🤝 Contributing

```bash
git checkout -b feature-name
git commit -m "Add feature"
git push origin feature-name
```

---

## 👨‍💻 Author

**Nitin Babu**
B.Tech CSE — Lovely Professional University

---

⭐ Star this repo if you found it useful!

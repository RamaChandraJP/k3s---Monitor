# ☸️ K3s Cluster Monitoring with Prometheus & Grafana 📊

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F5CFF?style=for-the-badge&logo=helm&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)

---

## 🚀 Overview

This project helps you **monitor your K3s Kubernetes cluster** using:

- 📈 **Prometheus** for metrics collection  
- 📊 **Grafana** for dashboards and visualization  

It includes all the commands from installing K3s to accessing dashboards in a **ready-to-copy cheat sheet**.

---

## 🛠️ Prerequisites

- ☸️ K3s cluster installed (single-node or multi-node)  
- 🖥️ `kubectl` configured  
- ⛵ Helm 3 installed  

---

## ⚡ Setup

All installation and configuration commands are available in the **Commands Cheat Sheet**:  

📄 [commands.md](./commands.md)

- The cheat sheet includes:  
  - K3s installation  
  - Helm setup  
  - Prometheus installation  
  - Grafana installation (NodePort exposed)  
  - Access instructions for dashboards  

---

## 🔑 Access Dashboards

- **Grafana**: `http://<NODE-IP>:<node-port>`  
  - Username: `admin`  
  - Password: (retrieved from `commands.md`)  

- **Prometheus**: `http://localhost:9090` (via port-forward)  

---


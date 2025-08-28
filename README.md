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

## 🏗️ Architecture

<img width="1061" height="700" alt="image" src="https://github.com/user-attachments/assets/3a0648b5-9f6c-4932-a8af-8d9a6dd04fd5" />


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

<img width="1893" height="858" alt="image" src="https://github.com/user-attachments/assets/54a632b5-e39f-47e8-ac09-f7c689c1665f" />


- **Prometheus**: `http://localhost:9090` (via port-forward)  

---


# K3s Kubernetes Monitoring with Prometheus & Grafana

This project provides an automated setup for monitoring a K3s Kubernetes cluster using Prometheus and Grafana, deployed with the [kube-prometheus-stack](https://github.com/prometheus-community/helm-charts) Helm chart.  
It’s designed for AWS EC2 (or any cloud server), and includes scripts to install K3s, deploy the monitoring stack, expose Grafana, and extract all Kubernetes YAML manifests for version control and reproducibility.

---

## Features

- **One-command setup:** Automated script to install K3s, Helm, Prometheus, and Grafana.
- **Cluster dashboards:** Get real-time metrics for nodes, pods, and apps.
- **Easy Grafana access:** NodePort exposure for browser-based dashboards.
- **Manifests for Git:** Extracts all generated Kubernetes YAML for auditing and sharing.
- **Beginner-friendly:** Simple, step-by-step, no prior experience needed.

---

## Prerequisites

- AWS EC2 instance (t3.small or higher recommended)
- Ubuntu 20.04+ (tested)
- Internet access for server

---

## Quick Start

Clone this repo and run the setup script (requires bash):


# Install K3s Cluster

curl -sfL https://get.k3s.io | sh -

sudo systemctl status k3s

# ================================
# Configure kubectl

export KUBECONFIG=/etc/rancher/k3s/k3s.yaml

kubectl get nodes

# ================================
# Install Helm (if not installed)

curl https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 | bash

helm version

# ================================
# Add Helm Repositories

helm repo add prometheus-community https://prometheus-community.github.io/helm-charts

helm repo add grafana https://grafana.github.io/helm-charts

helm repo update

# ================================
# Create Monitoring Namespace

kubectl create namespace monitoring

# ================================
# Install Prometheus

helm install prometheus prometheus-community/kube-prometheus-stack --namespace monitoring

# ================================
# Install Grafana with NodePort (to access externally)

helm install grafana grafana/grafana \
  --namespace monitoring \
  --set service.type=NodePort \
  --set service.nodePort=30080

# ================================
# Get Grafana admin password

kubectl get secret --namespace monitoring grafana -o jsonpath="{.data.admin-password}" | base64 --decode ; echo

# ================================
# Access Grafana via NodePort

# Open browser: http://<NODE-IP>:30080
# Username: admin
# Password: (from command above)

# ================================
# Access Prometheus (via port-forward)

kubectl get pods -n monitoring

kubectl port-forward service/prometheus-kube-prometheus-prometheus 9090:9090 -n monitoring

# Open browser: http://localhost:9090

# ================================
# Verify Cluster & Metrics

kubectl get pods -n monitoring

kubectl get nodes -o wide

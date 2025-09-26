# Prometheus Grafana


# Monitoring Setup with Prometheus & Grafana

## 📌 Overview
This repository provides an end-to-end setup of **Prometheus + Grafana** for monitoring Linux servers, Docker containers, and system metrics using **Node Exporter**.

---

## 🚀 Features
- 📡 **Prometheus**: Metrics collection and scraping
- 📈 **Grafana**: Real-time visualization dashboards
- 🖥️ **Node Exporter**: System metrics (CPU, Memory, Disk, Network)
- 🐳 **Docker Metrics**: Container-level monitoring
- ⚡ **Systemd Services**: Auto-start on boot

---

## 🏗️ Architecture
![Prometheus Setup](images/prometheus-setup.png)

---

## ⚡ Installation & Setup

### 1. Install Grafana
Steps to install Grafana and start the service.

### 2. Install Prometheus
Steps to install Prometheus, systemd service file, and configuration.

### 3. Install Node Exporter
Steps to install and configure Node Exporter service.

### 4. Configure Prometheus Targets
Example `prometheus.yml` file with node exporter and docker metrics.

### 5. Enable Docker Metrics
`/etc/docker/daemon.json` configuration.

---

## 📈 Grafana Dashboard
![Grafana Dashboard](images/grafana-dashboard.png)

- Add Prometheus as a data source
- Create dashboards & panels
- Example PromQL query for CPU usage:
  ```promql
  sum by(mode) (irate(node_cpu_seconds_total{mode!="idle"}[1m]))

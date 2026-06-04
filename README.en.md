# DCGM GPU Cluster Dashboard

English | [简体中文](README.md)

A production-ready Grafana dashboard for NVIDIA GPU clusters based on **DCGM Exporter**, **Prometheus**, and **Grafana**.

Designed for:

* AI Training
* LLM Inference
* Kubernetes GPU Clusters
* Slurm Clusters
* HPC Environments

---

## Dashboard Preview

### Cluster Overview

![Cluster Overview](screenshots/overview.png)

### GPU Inventory

![Cluster Table](screenshots/cluster_table.png)

### Alert Center

![Alert Center](screenshots/alerts.png)

---

## Features

| Overview           | Performance             | Health         |
| ------------------ | ----------------------- | -------------- |
| GPU Utilization    | Tensor Core Utilization | XID Errors     |
| Memory Utilization | GR Engine Active        | ECC Monitoring |
| GPU Temperature    | GPU Ranking             | Remapped Rows  |
| Power Usage        | Tensor Ranking          | Alert Timeline |

| Alert Center  | Analytics        | Inventory      |
| ------------- | ---------------- | -------------- |
| Abnormal GPUs | Memory Analysis  | GPU UUID       |
| Risk Ranking  | Thermal Analysis | GPU Model      |
| Hot GPUs      | PCIe / NVLink    | Driver Version |
| OOM Detection | Power Analysis   | PCI Bus ID     |

---

## Highlights

* 🚀 Cluster Overview
* 📊 GPU / Memory / Tensor Monitoring
* 🔥 Power & Thermal Analysis
* ❤️ Hardware Health Monitoring
* ⚠️ Intelligent Alert Center
* 🏆 GPU Risk Ranking
* 🔍 GPU Inventory Management
* 🌐 Multi-Node Cluster Support

---

## Compatibility

| Component  | Version |
| ---------- | ------- |
| DCGM       | 4.x     |
| Prometheus | 2.x+    |
| Grafana    | 11+     |

Recommended:

```yaml
nvidia/dcgm:4.5.2-1-ubuntu22.04
grafana/grafana:13.x
```

---

## Installation

1. Deploy DCGM Exporter
2. Configure Prometheus Scraping
3. Import the dashboard JSON
4. Select your Prometheus datasource

Dashboard file:

```text
dashboards/dcgm_gpu_cluster_dashboard.json
```

---

## License

Apache-2.0 License


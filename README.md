# DCGM GPU Cluster Dashboard

[English](README.en.md) | 简体中文

---

# 🚀 项目简介

一个面向 **AI / HPC GPU 集群** 的 NVIDIA DCGM Grafana 仪表盘。

基于：

* NVIDIA DCGM Exporter
* Prometheus
* Grafana

构建，专为：

* 大模型训练（LLM Training）
* 大模型推理（LLM Inference）
* Kubernetes GPU 集群
* Slurm GPU 集群
* HPC 集群

设计。

相比官方 Dashboard，本项目更偏向 **GPU 集群运维与资源运营**。

---

# 📸 Dashboard 预览

## 集群总览

![Cluster Overview](screenshots/overview.png)

---

## GPU 实时总览

![Cluster Table](screenshots/cluster_table.png)

---

## 性能分析

![Performance](screenshots/performance.png)

---

## 显存分析

![Memory](screenshots/memory.png)

---

## 功耗与温度分析

![Thermal](screenshots/thermal.png)

---

## 硬件健康

![Health](screenshots/health.png)

---

## 异常中心

![Alert Center](screenshots/alerts.png)

---

# ✨ 功能特性

## 集群总览

实时展示：

* GPU 平均利用率
* GPU 平均温度
* GPU 平均功耗
* GPU 平均显存利用率
* 活跃 GPU 数量
* 高温 GPU 数量
* 高显存 GPU 数量
* XID 异常 GPU 数量

---

## GPU 资产管理

实时 GPU 资产表：

* Instance
* Hostname
* GPU Index
* UUID
* GPU Model
* Driver Version
* PCI Bus ID

以及：

* GPU Util %
* Memory Util %
* Tensor Util %
* Power Usage
* GPU Temperature

支持：

* 排序
* 搜索
* 过滤
* 多集群查询

---

## 性能分析

支持：

* GPU Utilization Trend
* Tensor Core Utilization
* GR Engine Active
* Top GPU Ranking
* Top Tensor Ranking

适用于：

* PyTorch
* TensorFlow
* DeepSpeed
* Megatron-LM
* vLLM
* TensorRT

---

## 显存分析

显存利用率采用：

FB_USED / (FB_USED + FB_FREE)

计算。

无需依赖：

* DCGM_FI_DEV_FB_TOTAL

兼容更多 DCGM 环境。

---

## 功耗与温度

GPU 温度阈值：

| 温度   | 状态   |
| ---- | ---- |
| <80℃ | 正常   |
| ≥80℃ | 警告   |
| ≥85℃ | 高风险  |
| ≥90℃ | 严重告警 |

---

## 硬件健康

支持：

* XID 错误监控
* ECC 错误监控
* Remapped Rows
* PCIe 异常监控

---

## 异常中心

重点关注：

* 高温 GPU
* 高显存 GPU
* XID 异常 GPU
* 风险排行榜
* 历史异常趋势

帮助运维快速定位问题。

---

# 🎯 项目优势

### 集群优先设计

适用于：

* GPU Cluster
* Kubernetes GPU
* Slurm GPU
* AI Platform

---

### 高兼容性

支持：

* DCGM 4.x
* Grafana 11+
* Grafana 12+
* Grafana 13+
* Prometheus 2.x+

---

### 运维友好

快速回答：

* 哪张 GPU 正在工作？
* 哪张 GPU 即将 OOM？
* 哪张 GPU 温度过高？
* 哪张 GPU 存在 XID？
* 哪张 GPU 风险最高？

---

# 🛠 环境要求

推荐版本：

* nvidia/dcgm:4.5.2-1-ubuntu22.04
* grafana/grafana:13.x
* prometheus:2.x

---

# 📦 安装

1. 部署 DCGM Exporter
2. 配置 Prometheus 抓取
3. 导入 Dashboard JSON
4. 选择 Prometheus 数据源

即可开始监控 GPU 集群。

---

# 📄 License

Apache-2.0 License


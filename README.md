# High-Availability-Web-Ops
# 🚀 高可用 Web 集群运维实战 (High Availability Web Ops)

> **项目描述**：本项目模拟了企业级 Web 集群的从 0 到 1 搭建过程，涵盖架构设计、自动化部署、高可用配置、性能压测及可视化监控。

## 📋 项目背景
为了保障业务的高可用性，避免单点故障，本项目构建了一套基于 Nginx + Keepalived 的双机热备集群，并引入 Prometheus + Grafana 进行全方位监控。

## 🛠️ 技术栈
- **操作系统**: CentOS 7 / Ubuntu
- **负载均衡**: Nginx
- **高可用**: Keepalived
- **监控告警**: Prometheus, Grafana
- **自动化工具**: Ansible, Shell
- **压力测试**: Apache Bench (ab)

## 📊 核心成果展示

### 1. 架构设计
<img width="960" height="1280" alt="image_240078459681138" src="https://github.com/user-attachments/assets/5525d563-7f6f-43cb-b7ed-d7c1f4a76076" />


### 2. 高可用与负载均衡 (Keepalived + Nginx)
通过配置 Keepalived 实现主备切换，确保 VIP (虚拟 IP) 的漂移，保障服务不中断。
<img width="623" height="437" alt="屏幕截图 2025-12-25 104659" src="https://github.com/user-attachments/assets/60540e9a-ac26-4fda-9164-53cda1e7e716" />


### 3. 自动化运维 (Ansible)
编写 Playbook 实现批量配置下发，减少人工操作风险。

<img width="594" height="422" alt="屏幕截图 2025-12-25 115204" src="https://github.com/user-attachments/assets/d1cf9a04-3a02-49e7-bbd3-1f85d5afedeb" />


### 4. 性能压测 (Apache Bench)
在集群搭建完成后，进行压力测试以评估系统瓶颈。
- **并发数**: 1000
- **请求数**: 10000
<img width="594" height="422" alt="屏幕截图 2025-12-25 115204" src="https://github.com/user-attachments/assets/af25054b-e55d-4f5d-b489-9f23f6937208" />


### 5. 可视化监控 (Grafana)
搭建 Prometheus + Grafana 监控面板，实时展示服务器负载、Nginx 连接数等关键指标。
<img width="1253" height="707" alt="普罗米修斯可视化" src="https://github.com/user-attachments/assets/f90226ef-fd78-443e-b5e5-005e7267e669" />


## 📂 目录说明
- `Scripts/`: 包含自动化部署脚本。
- `Configs/`: 包含 Nginx 和 Prometheus 的核心配置片段。

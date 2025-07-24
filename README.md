# Centralized Monitoring Stack with Grafana, Loki, and Promtail

This project sets up a **centralized logging and monitoring system** using Dockerized components: **Grafana**, **Loki**, and **Promtail**. It collects logs from a file and visualizes them in real time using Grafana dashboards.

---

## 🔧 Stack Components

- **Grafana** – Visualization and alerting UI
- **Loki** – Log aggregation backend
- **Promtail** – Log shipper for Loki
- **Docker Compose** – To orchestrate services

---

## 📁 Folder Structure
central-monitoring-stack/
│
├── docker-compose.yml
├── README.md
├── .gitignore
│
├── prometheus/
│   └── prometheus.yml
│
├── grafana/
│   └── (Optional: datasources or dashboards json files)
│
├── loki/
│   ├── loki-config.yaml
│   ├── chunks/
│   ├── index/
│   ├── cache/
│   └── wal/
│
├── promtail/
│   └── promtail-config.yaml
│
└── logs/
    └── example.log  ← (custom log file for testing)

 What Each Folder Does:
docker-compose.yml: Runs all services.
prometheus/: Configuration for Prometheus.
grafana/: Optional configurations (like dashboards).
loki/: Config and data storage for Loki.
promtail/: Promtail config for log scraping.
logs/: A custom directory where Promtail reads logs (make sure this is mounted in Docker).



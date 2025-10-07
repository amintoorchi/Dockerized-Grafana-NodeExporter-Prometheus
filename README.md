<xaiArtifact artifact_id="22fdcd47-e48b-429a-9af2-28c2749a7456" artifact_version_id="6135213c-4bea-4017-b70b-8294a00aae9f" title="README.md" contentType="text/markdown">

# 📊 Prometheus, Node Exporter, and Grafana Dockerized

A powerful, Dockerized monitoring stack featuring **Prometheus**, **Node Exporter**, and **Grafana**. This project simplifies deployment and provides beautiful visualizations for system metrics. 

---

## ✨ Features

- **Prometheus**: Efficiently collects and stores system metrics. 
- **Node Exporter**: Exposes detailed hardware and OS metrics from your host. 
- **Grafana**: Creates stunning, customizable dashboards for data visualization. 
- **Persistent Storage**: Safely stores Prometheus and Grafana data. 
- **Docker Compose**: Enables quick setup with a single command. 

---

### 📋 Prerequisites

Ensure the following are installed on your system:

-  **Docker** (latest version recommended)
-  **Docker Compose** (version 3.8 or higher)

---

## 🚀 Installation !

Follow these steps to deploy the monitoring stack:

### 1. Clone the Repository

```bash
git clone https://github.com/username/repo-name.git
cd repo-name
```

### 2. Launch the Services

Start the containers in detached mode:

```bash
docker compose up -d
```

### 3. Access the Services

-  **Prometheus**: [http://localhost:9090](http://localhost:9090)
-  **Grafana**: [http://localhost:3000](http://localhost:3000)  
  *Default credentials*: `admin` / `admin` (update password after first login)

---

## 🛠️ Configuration

- **Docker Compose**: The `docker-compose.yml` is pre-configured. Customize ports or volumes as needed.
- **Grafana Dashboards**: Import pre-existing dashboards or create custom ones after logging in.
- **Storage**:
  - Prometheus data is stored in `./prom_data/`.
  - Grafana configurations are saved in `./grafana-storage/`.
  - Both directories are auto-created on first run and listed in `.gitignore`.

> **Note**: Add `./prom_data` and `./grafana-storage` to `.gitignore` to prevent uploading sensitive data to GitHub.

### Network Configuration

- **Host Network Mode**: Used by Node Exporter and Prometheus for direct access to host metrics.
- **Portability**: Switch to a `bridge` network in `docker-compose.yml` for cross-system compatibility.

---

###  Troubleshooting

Resolve issues with these steps:

- **View Logs**: Check container logs for errors:
  ```bash:disable-run
  docker compose logs
  ```
- **Port Conflicts**: Ensure ports `9090` (Prometheus) and `3000` (Grafana) are available.
- **Storage Permissions**: Verify that `./prom_data` and `./grafana-storage` have proper permissions.

---

### 🧭 Ready-to-use Grafana Dashboard

If you need a pre-built Grafana dashboard, you can use this beautiful and fully featured **Node Exporter Full** dashboard:

👉 [Grafana Dashboard #1860](https://grafana.com/grafana/dashboards/1860-node-exporter-full/)

---

##  Contributing

We welcome contributions to improve this project! To get started:

1.  Fork the repository.
2.  Create a feature or bug-fix branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3.  Commit your changes and push to your fork.
4.  Submit a pull request with a detailed description of your updates.

---

###  License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for more details.

---

### 🌟 Acknowledgments

- Built with ❤️ by Amin Toorchi
- Gratitude to the open-source community for their incredible tools and resources.

</xaiArtifact>
```

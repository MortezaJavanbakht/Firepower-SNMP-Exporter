# Firepower SNMP Exporter

This repository provides a comprehensive setup for monitoring Cisco Firepower firewalls using SNMP Exporter, integrated with Prometheus and Grafana. It includes configuration files for SNMP Exporter, Prometheus alerting rules, and a Grafana dashboard to visualize collected metrics.

## Features
- **SNMP Exporter Configuration**: Pre-configured settings to collect metrics from Cisco Firepower firewalls via SNMP.
- **Prometheus Alerting Rules**: Custom alert rules tailored for Firepower metrics to ensure proactive monitoring.
- **Grafana Dashboard**: A ready-to-use dashboard for visualizing Firepower metrics in Grafana.

## Prerequisites
- Prometheus server with SNMP Exporter module installed.
- Grafana instance for dashboard visualization.
- Cisco Firepower firewall configured to allow SNMP queries.
- Basic knowledge of Prometheus, SNMP, and Grafana.

## Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/MortezaJavanbakht/Firepower-SNMP-Exporter.git
   cd Firepower-SNMP-Exporter
   ```

2. **Configure SNMP Exporter**:
   - Copy the provided `snmp.yml` configuration file to your SNMP Exporter directory.
   - Update the file with your Firepower firewall's IP address and SNMP community string.

3. **Set Up Prometheus Alerts**:
   - Add the `alerts.yml` file to your Prometheus rules directory.
   - Reload Prometheus to apply the new alerting rules:
     ```bash
     curl -X POST http://<prometheus-host>:9090/-/reload
     ```

4. **Import Grafana Dashboard**:
   - In Grafana, navigate to **Dashboards** > **Import**.
   - Upload the `grafana_dashboard.json` file from this repository.
   - Configure the data source to point to your Prometheus instance.

## Usage
- Ensure SNMP Exporter is running and scraping metrics from the Firepower firewall.
- Verify that Prometheus is collecting metrics and triggering alerts based on the defined rules.
- Access the Grafana dashboard to monitor real-time metrics and visualize firewall performance.

## Directory Structure
```
Firepower-SNMP-Exporter/
├── snmp.yml              # SNMP Exporter configuration for Firepower
├── alerts.yml            # Prometheus alerting rules
├── grafana_dashboard.json # Grafana dashboard for Firepower metrics
└── README.md             # This file
```

## Contributing
Contributions are welcome! Please feel free to submit issues or pull requests for improvements or bug fixes.

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m "Add feature"`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For questions or support, please open an issue in this repository or contact [morteza.javanbakht@gmail.com](mailto:morteza.javanbakht@gmail.com).

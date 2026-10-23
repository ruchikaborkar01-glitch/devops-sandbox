Local DevOps Sandbox for Monitoring & Alerting
Overview
A Docker Compose-based monitoring and alerting project using Prometheus, Grafana, Alertmanager, Node Exporter, Blackbox Exporter, and Nginx.

Technologies Used
Docker Compose
Prometheus
Grafana
Alertmanager
Node Exporter
Blackbox Exporter
Nginx
Project Structure

devops-sandbox/
├── docker-compose.yml
├── README.md
├── .gitignore
├── prometheus/
│   ├── prometheus.yml
│   └── alert.rules.yml
├── alertmanager/
│   └── alertmanager.yml
├── grafana/
│   └── provisioning/
│       └── datasources/
│           └── datasource.yml
└── screenshots/
Services

Service	URL
Prometheus	http://localhost:9090
Grafana	http://localhost:3000
Alertmanager	http://localhost:9093
Node Exporter	http://localhost:9100/metrics
Blackbox Exporter	http://localhost:9115
Nginx	http://localhost:8080
Setup
Prerequisites
Docker Engine
Docker Compose plugin
Start the project

docker compose up -d
Check services

docker compose ps
Verify Prometheus targets
Open http://localhost:9090/targets

Access Grafana
Open http://localhost:3000

Use your configured Grafana credentials. Change default credentials before any public or production deployment.

Stop services

docker compose down
Monitoring and Alerting
Prometheus collects metrics from configured targets.
Alert rules are defined in prometheus/alert.rules.yml.
Alertmanager handles alerts sent by Prometheus.
Grafana provides dashboards for monitoring metrics.
Node Exporter exposes system metrics.
Blackbox Exporter supports endpoint probing.
Nginx provides a sample web service.
Screenshots
Add project screenshots to the screenshots/ directory.

Future Improvements
Validate alert notifications end to end.
Add Blackbox probe targets and test endpoint availability.
Improve dashboard coverage.
Pin Docker image versions for reproducible deployments.
Disclaimer
This project is for learning and demonstration. Review configuration and credentials before public or production use.

# Watch

This is monitoring the containers in the system with the use of [cAdvisor](https://github.com/google/cadvisor), [Prometheus](https://prometheus.io/), and [Grafana](https://grafana.com/).

## How to use

- Install [Docker](https://docs.docker.com/get-docker/).
- Run the monitoring orchestration in background: `docker compose up -d`
- View Grafana UI: [http://localhost:3333](http://localhost:3333)
- View cAdvisor: [http://localhost:8080](http://localhost:8080)
- View Prometheus : [http://localhost:9090](http://localhost:9090)
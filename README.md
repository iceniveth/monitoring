# Monitoring

This is monitoring the containers in the system with the use of [cAdvisor](https://github.com/google/cadvisor), [Prometheus](https://prometheus.io/), and [Grafana](https://grafana.com/) with [Docker Compose](https://docs.docker.com/compose/).

## How to use

- Install [Docker](https://docs.docker.com/get-docker/).
- Create a `.env` file with content:
  ```properties
  # Below is for the Grafana account
  GF_SECURITY_ADMIN_USER=admin
  GF_SECURITY_ADMIN_PASSWORD=password
  ```
- Run the monitoring orchestration in background: `docker compose up -d`
- View Grafana UI: [http://localhost:3000](http://localhost:3000)
- View cAdvisor: [http://localhost:8080](http://localhost:8080)
- View Prometheus : [http://localhost:9090](http://localhost:9090)

## Adding more dashboards in Grafana

They have a tons of repository of dashboards to choose from: [Grafana Dashboards](https://grafana.com/grafana/dashboards/). 
- View any then click the **Copy ID to clipboard**.
- Open the import Grafana dashboard page: http://localhost:3000/dashboard/import.
- Paste the Copied ID Dashboard to the **Dashboard URL or ID** field and then click **Load**.
- Select a Prometheus data source, then click **Import**.

That's done at this point. But if you want to contribute that dashboard in this repository:

- View that dashboard.
- Click the **Share** button (blue) in the top right section of the page.
- A dialog will pop up, head over to the **Export** tab.
- Click **Save to file**, name it and then save it under this repository `./grafana/dashboards`.

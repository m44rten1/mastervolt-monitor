# Mastervolt monitor

This application reads data from a Mastervolt system and stores it in an InfluxDB. Optionally, you can set up Grafana to view the data.

## Setup steps (linux)

Check if docker and docker-compose are installed:

```bash
$ docker --version
```

```
$ docker-compose --version
```

If not, install them:

```
sudo apt-get update -y
```

```
sudo apt install docker.io -y && sudo apt install docker-compose -y
```

Now,

```
docker-compose up
```

will spin up these containers:

- InfluxDB
- Grafana
- mastervolt-monitor

Connect grafana to InfluxDB in the grafana UI (http://localhost:8080) via the data sources and create desired dashboards. Settings:

- url: http://influxdb:8086
- organisation: m44rten1
- Token: `copy from influxDB UI`

# docker-prometheus

原项目: https://github.com/stefanprodan/dockprom

这是一个集成了 [Prometheus](https://prometheus.io/), [Grafana](http://grafana.org/),[NodeExporter](https://github.com/prometheus/node_exporter) and alertmanager [AlertManager](https://github.com/prometheus/alertmanager)的基于docker和容器的监控系统.


## 安装

克隆这个项目到你本地, cd到项目的根目录执行docker-compose up:

```bash
git clone https://github.com/jackqli/docker-promtheus
cd dockprom

ADMIN_USER=admin ADMIN_PASSWORD=admin ADMIN_PASSWORD_HASH=JDJhJDE0JE91S1FrN0Z0VEsyWmhrQVpON1VzdHVLSDkyWHdsN0xNbEZYdnNIZm1pb2d1blg4Y09mL0ZP docker-compose up -d
```

前提条件:

* Docker Engine >= 1.13
* Docker Compose >= 1.11


容器:

* Prometheus (metrics database) `http://<host-ip>:9090`
* Prometheus-Pushgateway (push acceptor for ephemeral and batch jobs) `http://<host-ip>:9091`
* AlertManager (alerts management) `http://<host-ip>:9093`
* Grafana (visualize metrics) `http://<host-ip>:3000`
* NodeExporter (host metrics collector)
* Caddy (reverse proxy and basic auth provider for prometheus and alertmanager)


![Host](https://raw.githubusercontent.com/jackqli/dockprom/master/screens/Grafana_Docker_Host2.png)


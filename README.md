# docker-swarm-monitor

Docker-swarm-monitor is a container monitoring solution for [Docker Swarm](https://docs.docker.com/engine/swarm/).
It uses [Docker Compose](https://docs.docker.com/compose/overview/) with **multi-architecture** Docker images for [Node exporter](https://github.com/prometheus/node_exporter), [cAdvisor](https://github.com/google/cadvisor), [Prometheus](https://github.com/prometheus/prometheus) and [Grafana](https://github.com/grafana/grafana).

## How to use

Clone this repository on your host pc that serves as a manager node in your Docker swarm.
Then just deploy the stack with the following command

    docker stack deploy --compose-file docker-compose.yml prom

Now you can access the web interfaces exposed by Prometheus and Grafana using the manager node's IP address and the corresponding port numbers (3000 for Grafana, 9090 for Prometheus).

## General information

The included dashboard and also the configuration are optimized for low resource utilization in order to allow the deplyoment on ARM SBCs like the Raspberry Pi 2 or 3(+).

Please note that this project is only intended for test purposes.


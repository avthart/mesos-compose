# mesos-compose
Run a Dockerized Mesos and Marathon environment on your own machine so that you can develop and test locally. Weave Scope is installed for visualizing, monitoring and controlling your mesos/docker infrastructure (containers, processes, networks, etc.)

Versions:

* Mesos 0.27.0
* Marathon 0.15.1
* Weave Scope 0.13.1

# Boot the infrastructure

## Prerequisites
- If you have installed the Docker Toolbox (Mac OS X / Windows): Change the MESOS_HOSTNAME in docker-compose.yml to the IP-address of your Docker Machine `docker-machine ip`.

- If you use a linux host (make sure that you have [docker-compose](https://docs.docker.com/compose/install/) installed): Change the MESOS_HOSTNAME in docker-compose.yml to the local IP-address of your computer. You can find this IP by `ip addr | grep "inet "`, choose the IP after the `lo` adapter.

## Start mesos and marathon
You can start mesos and marathon using Docker Compose:

```
docker-compose up -d
```

User Interfaces:

* Marathon http://DOCKER_MACHINE_IP:8080/
* Mesos http://DOCKER_MACHINE_IP:5050/
* Weave Scope http://DOCKER_MACHINE_IP:4040/

# Traefik HTTP router

You can optionally run Traefik as a HTTP (Edge) router. See https://github.com/emilevauge/traefik

```
docker-compose -f traefik-compose.yml up -d
```

User Interfaces:
* Traefik Admin http://DOCKER_MACHINE_IP:10080/

# Consul

You can optionally run Consul for Service Discovery
```
docker-compose -f consul-compose.yml up -d
```

User Interfaces:
* Consul UI http://DOCKER_MACHINE_IP:8500/

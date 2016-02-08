# mesos-compose
Run a Dockerized Mesos and Marathon environment on your own machine so that you can develop and test locally.

Versions:

* Mesos 0.27
* Marathon 0.15
* Docker 1.9

# Boot the infrastructure
We assume that you have installed the Docker Toolbox.

Change the MESOS_HOSTNAME in docker-compose.yml to the IP-address of your Docker Machine

> docker-machine ip

You can start mesos and marathon using Docker Compose:

> docker-compose up -d

# Interfaces

* Marathon http://DOCKER_MACHINE_IP:8080/
* Mesos http://DOCKER_MACHINE_IP:5050/

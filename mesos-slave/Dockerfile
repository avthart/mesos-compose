FROM mesosphere/mesos-slave:0.27.0-0.2.190.ubuntu1404
RUN apt-get update
RUN apt-get -y install curl
RUN curl -sSL -o /usr/bin/docker https://get.docker.com/builds/Linux/x86_64/docker-1.9.1
RUN chmod +x /usr/bin/docker
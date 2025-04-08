# 07. Docker

## Homework Assignment 1: Docker Installation and Basic Commands
1. Go to:  https://docs.docker.com/engine/install/debian/
2. Follow the instruction:
```bash
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
3. Execute: ```docker --version```
```bash
Output:Docker version 28.0.4, build b8034c0
```
4.  Pull the official "hello-world" Docker image and run a container based on it.
```bash

> sudo docker run hello-world

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
```

5. List of containers.
```bash
debian@vbox ~/i/07.Docker (master)> docker ps -a
CONTAINER ID   IMAGE         COMMAND    CREATED          STATUS                      PORTS     NAMES
70331da05011   hello-world   "/hello"   2 minutes ago    Exited (0) 2 minutes ago              recursing_bose
8d2519c9321e   hello-world   "/hello"   15 minutes ago   Exited (0) 15 minutes ago             keen_moore
```

## Homework Assignment 2: Building a Docker Image with Dockerfile

# Staructure of project
.  
|-- app.py
|-- Dockerfile  
|-- requirements.txt  
|-- nginx.conf

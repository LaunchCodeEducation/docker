---
title: "Docker Images"
date: 2021-10-01T09:28:27-05:00
draft: false
---

## Docker Images

Docker images can be stored and accessed through Dockerhub. Think of Dockerhub similar to how you would think about Github storing project repositories.

Dockerhub will store images or snapshots of any given project that you can access as long as they are not private in nature.

Similar to most tutorials and introductions to new technologies the `Digital Ocean` walkthrough suggests we attempt to grab a `hello-world` image from Dockerhub.

In the above example we currently do not have the `hello-world` image locally on our machine. The `docker run` command states the following:

- `docker run: Run a command in a new container`. If you do not already have the image it will download and pull the image from dockerhub and finally run the image in a new container on your machine.

```bash
docker run hello-world
```

![docker-hello-world](pictures/docker-run-hello-world.png?classes=border)

### Viewing Downloaded Images

```bash
sudo docker images
```

![docker-images-command](pictures/docker-images.png?classes=border)

## Other useful commands
1. `docker ps`: view active containers
1. `docker ps -a`: view all containers (active or inactive)
1. `docker ps -l`: view last container created
1. `docker start <container name, id>`: start a stopped container
1. `docker rm`: remove a stopped container


---
title: "Docker Installation"
date: 2022-05-11T15:46:05-05:00
draft: false
weight: 105
---

## Installing and Using Docker with Ubuntu 22.04

## Resources
- [Docker Documentation](https://docs.docker.com/)
- [Digital Ocean Walkthrough](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-22-04)

### Installing Docker
```bash
sudo apt update -y

sudo apt install apt-transport-https ca-certificates curl software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update -y

apt-cache policy docker-ce

sudo apt install docker-ce
```

### Verify Installation

```bash
which docker
```

```bash
docker --version
```

### Check docker status with systemd

```bash
sudo systemctl status docker
```

![Docker Status](pictures/docker-status.png?classes=border)

### View Current Info of Docker Images and Containers

```bash
sudo docker info
```


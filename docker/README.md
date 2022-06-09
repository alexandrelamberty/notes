---
author: Alexandre Lamberty
title: Docker
description: | 
Set of platform as a service products that use OS-level virtualisation to
deliver software in packages called containers
category: Software
tags: [container,virtualisation,image]
created: 2021-11-11T17:30:39+01:00
updated: 2021-11-11T17:30:39+01:00
---

# Docker

## Installation

### Users, Groups and Permissions

```bash
sudo usermod -aG docker $USER
```

> Check this command

```bash
sudo newgrp docker
```

```bash
sudo chmod 666 /var/run/docker.sock
```

## Usage

Enter a running container

```bash
docker exec -it [container-id] bash
```

## Volumes

```bash
docker-compose down --volumes
```

## Network

https://docs.docker.com/network/bridge/#enable-forwarding-from-docker-containers-to-the-outside-world

## Formatting

```bash
docker container ls --all --format '{{.Names}}'
```

## References

<https://docs.docker.com/config/formatting/>
[](https://docs.docker.com/engine/swarm/)
[Portainer](www.portainer.io)

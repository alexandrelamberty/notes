---
author: Alexandre Lamberty
title: Sshfs
description: |
 Filesystem client to mount and interact with directories and files located on
 a remote server or workstation over a normal ssh connection
category: Software
tags: ["sshfs","ssh","file-system","secure","protocol","network","server","linux"]
created: 2021-04-06T13:34:30+02:00
updated: 2021-04-06T13:34:30+02:00
---
# Sshfs

A network filesystem client to connect to SSH servers.

## Usage

Mount filesytem from remote with login.

```bash
sudo sshfs -o allow_other,default_permissions root@xxx.xxx.xxx.xxx:/ /mnt/droplet
```

Mount filesystem from remote ssh key authorization
```bash
sudo sshfs -o allow_other,default_permissions,IdentityFile=~/.ssh/id_rsa root@xxx.xxx.xxx.xxx:/ /mnt/droplet
```

## Permanent mounting

Edit your `/etc/fstab` file.

Add a ligne correspinding to the desired mounting fs


sshfs#root@xxx.xxx.xxx.xxx:/ /mnt/droplet

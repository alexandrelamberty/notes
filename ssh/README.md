---
author: Alexandre Lamberty
title: SSH - Secure Shell
description: |
  Cryptographic network protocol for operating network services securely over an
  unsecured network
category: Linux
tags: ['ssh', 'secure', 'shell', 'protocol', 'network', 'linux']
created: 2021-04-06T13:34:30+02:00
updated: 2021-04-06T13:34:30+02:00
---

# Ssh

> Check cryptographic network protocol meaning

## Configuration

## Generating a new SSH Key

Key are used to manage
Create a Private/Public Key on your local machine

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Copy public Key on the remote server

```bash
ssh-copy-id user@
```

## Adding your SSH Key to the ssh-agent

Start the ssh-agent

```bash
$ eval "$(ssh-agent -s)"
> Agent pid 59566
```

Add your private key to the ssh-agent

```bash
$ ssh-add ~/.ssh/id_ed25519
```

---
author: Alexandre Lamberty
title: Scp - Secure Copy Protocol 
description: Copies files between hosts on a network
category: Software
tags: ["scp","copy","file","secure","protocol","network","linux"]
created: 2021-04-06T13:34:30+02:00
updated: 2021-04-06T13:34:30+02:00
---
# Scp - Secure Copy Protocol

Secure Copy Protocol

```bash
scp source destination
```

## Copy from local host A to remote host B

```bash
scp source user@host:destination
```

## Copy from remote host B to local host A

```bash
scp user@host:source destination
```

## Copy from remote host A to remote host B

```bash
scp user@host:source user@host:destination
```

## References

- [OpenSSH](https://www.openssh.com/)



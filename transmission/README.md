---
author: Alexandre Lamberty
title: Transmissions-cli
description: A fast, and free BitTorrent client
category: Torrent
tags: ["transmission","torrent","cli"]
created:  2021-11-22T21:24:54+01:00
updated: 2021-11-22T21:24:54+01:00
---
# Transmission

A fast, and free BitTorrent client.

## Configuration

Show the configuration

```bash
transmission-daemon --dump-settings
```

Change the download directory 

```bash
transmission-daemon --download-dir "directory-path"
```

## Start the transmission deamon

> See if a service is not installed and running by default when installing the software.

```bash
transmission-daemon
```
## Adding a torrent

You can add torrent as file from server:

```bash
transmission-remote -a ".torrent"
```

or as P2P magnet

```bash
transmission-remote -a "magnet:"
```

## Download status

Check the status of you downloads

```bash
transmission-remote -l
```

You can `watch` the output of the command to have a continuous 
progress overview. See: [watch](../watch/)

```bash
watch -n 5 transmission-remote -l
```

## Removing a torrent

Remove the torrent with the ID 1

```bash
transmission-remote -t 1 -r
```

Remove multiple torrents

```bash
transmission-remote -t 2,3 -r
```

Remove all torrents

```bash
transmission-remote -t all -r
```

## Web UI

Transmissions-deamon

## References

- [Transmission](https://transmissionbt.com/)

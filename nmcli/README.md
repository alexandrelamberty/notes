---
author: Alexandre Lamberty
title: Nmcli
description: | Command-line tool for controlling NetworkManager and reporting
network status
category: Linux
tags: [network,ethernet,wifi,cli,linux]
created: 2021-04-06T13:34:30+02:00
updated: 2021-04-06T13:34:30+02:00
---

# Nmcli

Check status of your device

```bash
nmcli dev status
```

Check if wifi is enable

```bash
nmcli radio wifi
```

Enable wifi

```bash
nmcli radio wifi on
```

List wifi network

```bash
nmcli dev wifi list
```

Connect to a wifi network

```sh
nmcli dev wifi connect [ssid] password [password]
```

Disconnect from network

```bash
nmcli con dow [network]
```

## References

- [NetworkManager - ArchWikbv ](https://wiki.archlinux.org/title/NetworkManager)

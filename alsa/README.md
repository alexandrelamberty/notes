---
author: Alexandre Lamberty
title: Alsa (Advanced Linux Sound Architecture)
description: | 
Provides an application programming interface for sound card device drivers
category: Software
tags: [audio,sound,linux]
created: 2021-11-11T17:30:39+01:00
updated: 2021-11-11T17:30:39+01:00
---
# Alsa (Advanced Linux Sound Architecture)

## Configuration

Checking USB device

```bash
udevadm monitor --udev
```

Write you device path ex:

```
/devices/pci0000:00/0000:00:1d.0/usb2/2-1/2-1.2/2-1.2:1.1`
```

Find device info

```bash
udevadm info --path=/your/device/path --attribute-walk
```

### Asoundrc

## Commands 

### Restore

```bash
alsactl restore
```

## References

- [ALSA Project](https://www.alsa-project.org)
- [ALSA - ArchWiki](https://wiki.archlinux.org/title/Advanced_Linux_Sound_Architecture)

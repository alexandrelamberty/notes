---
author: Alexandre Lamberty
title: DD
description: Copy and convert files
category: Software
tags: [copy, convert, files, iso, usb]
created: 2021-10-29T15:34:06+02:00
updated: 2021-10-29T15:34:06+02:00
---

# DD

Copy and convert files.

## Bootable USB

```bash
sudo dd if=your_iso.iso of=/dev/device_name bs=1M status=progress
```

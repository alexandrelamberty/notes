---
author: Alexandre Lamberty
title: TP-Link Archer T2U PLUS 
description: Wireless Dual Band USB Adapter
category: Device
tags: ["linux","driver","usb","wifi"]
created: 2021-10-23T20:42:15+02:00
updated: 2021-12-21T18:05:22+02:00
---
# TP-Link Archer T2U PLUS [RTL8821AU]

This breaks all the time with the last kernel updates.

> ! Make a pacman hooks to stop from updating the drivers 
> ! Check pacman conf IgnorePkg

## Drivers
- [8821au](https://github.com/morrownr/8821au-20210708.git)
- [rtl8812au-dkms-git](https://aur.archlinux.org/rtl8812au-dkms-git.git)
- [rtl88xxau-aircrack-dkms-git](https://aur.archlinux.org/rtl88xxau-aircrack-dkms-git.git)

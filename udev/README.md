---
author: Alexandre Lamberty
title: Udev 
description: Device manager for the Linux kernel
category: Software
tags: ["udev","subsystem","event","device","manager","linux"]
created: 2021-04-06T13:34:31+02:00
updated: 2021-04-06T13:34:31+02:00
---
# Udev

## Commands 

Monitoring events
```bash
udevadm monitor -k -u -p
```

Reloading rules
```bash
udevadm control --reload
```

Manually force to trigger rules
```bash
udevadm trigger
```


## USB

### Use lsblk to get the usb name

```sh
lsblk
```

You will get something similar to this.

```sh
NAME   MAJ:MIN RM   SIZE RO TYPE MOUNTPOINT
sda      8:0    0 223.6G  0 disk
├─sda1   8:1    0   200M  0 part /boot
...
sdb      8:16   0  59.6G  0 disk
├─sdb1   8:17   0   651M  0 part
└─sdb2   8:18   0    64M  0 part
```

My usb device name is the first partition of my second disk
i.e. sdb1

You access your drives via `/dev`

### Then use blkid to get the usb uuid

```sh
sudo blkid /dev/device_name
```

Output:

```sh
/dev/sdb1: BLOCK_SIZE="2048" UUID="2020-03-01-09-32-57-00" LABEL="ARCH_202003" TYPE="iso9660" PTUUID="3372b9d9" PTTYPE="dos" PARTUUID="3372b9d9-01"
```

### Udev monitor

Execute

```sh
udevadm monitor --udev
```

then plug the usb and wait to see informations.

```sh
/devices/pci0000:00/0000:00:1d.7/usb1/1-5/1-5:1.0
```

```sh
udevadm info --path=/your/device/path --attribute-walk
```

```sh
...
ATTR{idVendor} 5567
ATTR{idProduct} 0781
...
```

## Rule

`/etc/udev/rules.d/`

CD
`95-usb-backup.rules`

```sh
KERNEL=="sd*", ACTION=="add", ATTR{serial}=="1", \
    RUN+="/home/eevos/.scripts/system-usb-udev.sh --update"
KERNEL=="sd*", ACTION=="remove", \
    RUN+="/home/eevos/.scripts/system-usb-udev.sh --update"
```

USB disk
`95-usb-backup.rules`

```sh
KERNEL=="sd*", ACTION=="add", ATTR{serial}=="1", \
    RUN+="/home/eevos/.scripts/system-usb-udev.sh --update"
KERNEL=="sd*", ACTION=="remove", \
    RUN+="/home/eevos/.scripts/system-usb-udev.sh --update"
```

SDC Cards
`95-sd-pictures.rules`

```sh
KERNEL=="sd*", ACTION=="add", ATTR{removable}=="1", \
    RUN+="/home/eevos/.scripts/system-usb-udev.sh --update"
KERNEL=="sd*", ACTION=="remove", \
    RUN+="/home/eevos/.scripts/system-usb-udev.sh --update"
```

### Execute what you want

```sh
notify⁻send "USB xxx Plugged in"
```

## Reload udev rules

```sh
udevadm control --reload
```

## References
- http://reactivated.net/writing_udev_rules.html
- https://www.pcsuggest.com/run-shell-scripts-from-udev-rules/
- http://www.reactivated.net/writing_udev_rules.html
- https://devconnected.com/how-to-mount-and-unmount-drives-on-linux/#:~:text=To%20mount%20the%20%E2%80%9Csda1%E2%80%9D%20partition%2C%20use%20the%20%E2%80%9Cmount,mountpoint%E2%80%9D%20in%20the%20home%20directory.&text=If%20you%20did%20not%20get,drive%20partition%20was%20successfully%20mounted!
- https://unix.stackexchange.com/questions/116536/call-notify-send-from-an-udev-rule
- https://github.com/tpm2-software/tpm2-abrmd/issues/132
- https://wiki.archlinux.org/index.php/Udev
- https://opensource.com/article/18/11/udev#:~:text=A%20udev%20rule%20must%20contain,this%20is%20a%20removable%20device.

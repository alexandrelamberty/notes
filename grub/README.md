---
author: Alexandre Lamberty
title: Grub 
description: Boot loader package
category: Linux
tags: ["grub", "linux", "partition"]
created: 2021-04-06T13:34:30+02:00
updated: 2021-04-06T13:34:30+02:00
---
# Grub

This is the beast in your nightmares ^^

## Introduction

Boot from ISO - Mapped to CD

find --set-root /archlinux-2014.12.01-dual.iso
map /archlinux-2014.12.01-dual.iso (hd32)
map --hook
root (hd32)
chainloader (hd32)

Archlinux heads

find --set-root /archlinux-2014.12.01-dual.iso
map --heads=0 --sectors-per-track=0 /archlinux-2014.12.01-dual.iso (0xff)
map --hook
root (0xff)
chainloader (0xff)

Archlinux mapped

find --set-root /archlinux-2014.12.01-dual.iso
map --heads=0 --sectors-per-track=0 /archlinux-2014.12.01-dual.iso (hd32)
map --hook
root (hd32)
chainloader (hd32)

## References

http://download.gna.org/grub4dos/
http://www.rmprepusb.com/tutorials/grub4dos

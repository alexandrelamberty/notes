---
author: Alexandre Lamberty
title: Pacman 
description: | Package manager for the arch Linux and arch-based Linux
distributions
category: Package manager
tags: [package,manager,arch-linux,arch-based]
created: 2021-04-06T13:34:31+02:00
updated: 2021-04-06T13:34:31+02:00
publish:
---

# Pacman

## Installing packages

```bash
$ pacman -S package_name
```

## Removing packages

```bash
$ pacman -R package_name
```

```bash
$ pacman -Rs package_name
```

Remove all uninstalled package

```bash
$ sudo pacman -Sc
```

## Cache

Get the number of package

```bash
$ sudo ls /var/cache/pacman/pkg/ | wc -l
```

Get the size it take on disk

```bash
$ du -sh /var/cache/pacman/pkg/
```

Remove packages keeping 3 downgrade versions

```bash
$ sudo paccache -r
```

List package by size

```bash
LC_ALL=C pacman -Qi | awk '/^Name/{name=$3} /^Installed Size/{print $4$5, name}' | sort -h
```

## Hooks

Create a file `/etc/pacman.d/hooks/clean_package_cache.hook`

```dosini
[Trigger]
Operation = Upgrade
Operation = Install
Operation = Remove
Type = Package
Target = *
[Action]
Description = Cleaning pacman cache...
When = PostTransaction
Exec = /usr/bin/paccache -r
```

## Rollback

## Listing packagaes

List packages installed from the arch repository.

```shell
pacman -Qnq
```

List packages installed from the AUR.

```shell
pacman -Qqem
```

## Invalid / corrupted packages

```bash
pacman -Sy archlinux-keyring
```

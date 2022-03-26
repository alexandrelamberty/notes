---
author: Alexandre Lamberty
title: Tmux 
description: |
 Open-source terminal multiplexer for Unix-like operating systems. It allows
 multiple terminal sessions to be accessed simultaneously in a single window.
 It is useful for running more than one command-line program at the same time
category: Software
tags: ["tmux", "terminal", "multiplexer", "linux"]
created: 2021-04-06T13:34:30+02:00
updated: 2021-04-06T13:34:30+02:00
---
# Tmux

## Configuration

See my [.tmux.conf]().

## Keybinds

## Pane Spliting

## Pane Switching

```conf
# switch panes using Alt-arrow without prefix
bind -n M-Left select-pane -L
bind -n M-Right select-pane -R
bind -n M-Up select-pane -U
bind -n M-Down select-pane -D
```

## Custom Behaviours

Don't rename windows automatically

set-option -g allow-rename off

## Visual customization

## Sessions

Tmux Resurect

# References

- [Tmux - ArchWiki](https://wiki.archlinux.org/title/tmux)
- [Maciakl - Dotfiles](https://github.com/maciakl/.dotfiles/blob/master/.tmux.conf)
- [John Murray - Dotfiles](https://github.com/JohnMurray/dotfiles/blob/master/.tmux.conf)

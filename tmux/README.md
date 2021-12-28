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

## Keybinds

## Pane Spliting

## Pane Switching

```
# switch panes using Alt-arrow without prefix
bind -n M-Left select-pane -L
bind -n M-Right select-pane -R
bind -n M-Up select-pane -U
bind -n M-Down select-pane -D
```

## Scrolling vi / emacs mode

Function                     vi              emacs
--------                     --              -----
Half page down               C-d             M-Down
Half page up                 C-u             M-Up
Next page                    C-f             Page down
Previous page                C-b             Page up
Scroll down                  C-Down or C-e   C-Down
Scroll up                    C-Up or C-y     C-Up
Search again                 n               n
Search again in reverse      N               N
Search backward              ?               C-r
Search forward               /               C-s

## Custom Behaviours

# don't rename windows automatically

set-option -g allow-rename off

## Visual customization

# References

- [Tmux - ArchWiki](https://wiki.archlinux.org/title/tmux)
- [Maciakl - Dotfiles](https://github.com/maciakl/.dotfiles/blob/master/.tmux.conf)
- [John Murray - Dotfiles](https://github.com/JohnMurray/dotfiles/blob/master/.tmux.conf)

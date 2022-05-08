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

## Installation

## Package manager

Default plugins location

## Sessions

List sessions with options
```bash
tmux ls -F "#{session_name}"
```

Use FZF to list sessions and attach to one
```bash
tmux attach-session -t $(tmux ls -F "#{session_name}" | fzf)
```

Kill all sessions
```bash
tmux list-sessions | awk 'BEGIN{FS=":"}{print $1}' | xargs -n 1 tmux kill-session -t
```

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

Tmux Resurect

# References

- [Tmux - ArchWiki](https://wiki.archlinux.org/title/tmux)
- [Tmux Package manager](https://github.com/tmux-plugins/tpm)
- [Tmux Resurrect](https://github.com/tmux-plugins/tmux-resurrect)
- [Tmux Continuum](https://github.com/tmux-plugins/tmux-continuum)
- [Maciakl - Dotfiles](https://github.com/maciakl/.dotfiles/blob/master/.tmux.conf)
- [John Murray - Dotfiles](https://github.com/JohnMurray/dotfiles/blob/master/.tmux.conf)

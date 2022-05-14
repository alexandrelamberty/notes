---
author: Alexandre Lamberty
title: Bash (Bourn Again Shell) 
description: Unix shell and command language
category: Software
tags: [shell,linux]
created: 2021-04-06T13:34:30+02:00
updated: 2021-04-06T13:34:30+02:00
---
# Bash

## Moving

| Syntax | Description |
| ----------- | ----------- |
|`Ctrl + a` | Go to beginning of line |
|`Ctrl + e` | Go to end of line |
|`Alt + f` | Move forward one word |
|`Alt + b` | Move back one word |
|`Ctrl + f` | Move forward one char |
|`Ctrl + b` | Move back one char |
|`Ctrl + u` | Delete characters left of the cursor |
|`Ctrl + k` | Delete characters right of the cursor |
|`Ctrl + w` | Delete the word left of the cursor |
|`Ctrl + d` | Delete the word to the left of the cursor |
|`Ctrl + \_` | Undo |
|`Ctrl + r` | History search (multiple time to cycle through resul) |
|`Arrow Up` | History commands older |
|`Arrow Down` | History commands newer |
|`Ctrl + y` | Paste |
|`Alt + l` | Lower case the current word after cursor |
|`Alt + u` | Upper case the current word after cursor |
|`Alt + c` | Capitalize current word after cursor |
|`Ctrl + l` | Clear terminal screen |
|`Ctrl + Alt + F?` | Exit terminal session |

## Navigation

pushd Go to destination
popd Get back from destination

## Bash Commands

## Bash Aliases

## Completion 

Bash completion allow you to dynamicaly complete bash commands.

View an example [tmux-bash-completion](https://github.com/imomaliev/tmux-bash-completion/blob/master/completions/tmux)

## Autocorrection

## Prompt

```
d - the date in "Weekday Month Date" format (e.g., "Tue May 26")
e - an ASCII escape character (033)
h - the hostname up to the first .
H - the full hostname
j - the number of jobs currently run in background
l - the basename of the shells terminal device name
n - newline
r - carriage return
s - the name of the shell, the basename of $0 (the portion following the final slash)
t - the current time in 24-hour HH:MM:SS format
T - the current time in 12-hour HH:MM:SS format
@ - the current time in 12-hour am/pm format
A - the current time in 24-hour HH:MM format
u - the username of the current user
v - the version of bash (e.g., 4.00)
V - the release of bash, version + patch level (e.g., 4.00.0)
w - Complete path of current working directory
W - the basename of the current working directory
! - the history number of this command
# - the command number of this command
$ - if the effective UID is 0, a #, otherwise a $
nnn - the character corresponding to the octal number nnn
\ - a backslash
[ - begin a sequence of non-printing characters, which could be used to embed a terminal control sequence into the prompt
] - end a sequence of non-printing characters
```
## References

- [Bash - GNU Project](https://www.gnu.org/software/bash/)
- https://mehmandarov.com/navigating-and-editing-the-command-line/qdfqs
- https://cameronnokes.com/blog/the-most-useful-bash-commands-for-front-end-development/
- https://misc.flogisoft.com/bash/tip_colors_and_formatting
- https://www.ostechnix.com/hide-modify-usernamelocalhost-part-terminal/

---
author: Alexandre Lamberty
title: MPV 
description: | Free and open-source media player software based on MPlayer,
mplayer2 and FFmpeg
category: Linux
tags: [video,player,linux]
created: 2021-04-06T13:34:30+02:00
updated: 2021-04-06T13:34:30+02:00
---

# MPV

## Configuration

User specific

`~/.config/mpv/mpv.conf`

```conf
globbal (default) options
loop-playlist=inf
loop-file=inf
# "finite" playback profile (disable looping)
# usage: mpv --profile=finite ...
# Note that "finite" is an arbitrary name
[finite]
loop-playlist=no
loop-file=no
```

## References

- [MPV](https://mpv.io/)

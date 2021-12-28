---
author: Alexandre Lamberty
title: Xwinwrap
description: X11 Window in desktop enviroment background 
tags: ["linux","x11","window","wrapper","utils"]
category: Linux
created: 2021-10-23T20:38:59+02:00 
updated: 2021-10-23T20:38:59+02:00
---
# Xwinwrap

## Usages

### Video background

```bash
xwinwrap -b -s -fs -st -sp -nf -ov -fdt \
	-- mpv -wid WID \
	--really-quiet --framedrop=vo \
	--no-audio --panscan="1.0" \
	/path/to/your/video
```

```bash
_screen() {
xwinwrap -ov -ni -g "$1" -- mpv --fullscreen\
	--no-stop-screensaver \
		--vo=vdpau --hwdec=vdpau \
		--loop-file --no-audio --no-osc --no-osd-bar -wid WID --no-input-default-bindings \
		"$2" &
	PIDs+=($!)
}
```

## References

- [Xwinwrap](https://github.com/mmhobi7/xwinwrap)
- https://doc.ubuntu-fr.org/xwinwrap

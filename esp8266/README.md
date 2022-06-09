---
author: Alexandre Lamberty
title: Esp8266
description: Cross-plateform software framework
category: Electronics
tags: [cross-plateform, javascript]
created: 2021-11-22T21:24:54+01:00
updated: 2021-11-22T21:24:54+01:00
---

# Esp8266

## NodeMCU LUA Amica V2 with ESP8266 12E

# Communication

You can use different software to do that. eg :

- [Minicom](https://linux.die.net/man/1/minicom)

- [Piocom](https://linux.die.net/man/8/picocom)

115,200 baud (-b 115200)
8 bits (default setting)
no parity (default setting)
no flow control (default setting)
and with no port reset (-r) and no port locking (-l),
use:

```bash
picocom -b 115200 -r -l /dev/ttyUSB0
```

To exit picocom, use CNTL-A followed by CNTL-X.

### Programming


## References

<https://github.com/esp8266>
<https://github.com/nodemcu>
<https://www.espressif.com/en/products/socs/esp8266>
<https://docs.espressif.com/projects/esptool/en/latest/esp8266/index.html>
<https://nodemcu.readthedocs.io>
<https://www.youtube.com/watch?v=v-pnV2sepxs>

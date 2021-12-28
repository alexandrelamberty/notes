---
author: Alexandre Lamberty
title: Ffmpeg
description: |
 Free and open-source software project consisting of a suite of libraries and
 programs for handling video, audio, and other multimedia files and streams 
category: Video
tags: ["dfmpeg","video","sound","webcam","editing"]
created: 2021-11-11T17:30:39+01:00
updated: 2021-11-11T17:30:39+01:00
---
# Ffmpeg

## Tests

```bash ffmpeg -f v4l2 -i /dev/video0 -preset ultrafast -vcodec libx264 -tune
zerolatency -b 900k -f flv rtmp://192.168.1.25:5000
```

```bash ffmpeg -f v4l2 -i /dev/video0 -preset ultrafast -vcodec libx264 -tune
zerolatency -b 900k -f flv -listen 1 -i rtmp://192.168.1.25:5000/live/app
```

```bash ffmpeg -f dshow -i /dev/video0 -profile:v high -pix_fmt yuvj420p
-level:v 4.1 -preset ultrafast -tune zerolatency \ -vcodec libx264 -r 10 -b:v
512k -s 640x360 \ -f mpegts -flush_packets 0
udp://192.168.1.4:5000?pkt_size=1316
```

```bash ffmpeg -f dshow -i /dev/video0 -profile:v high -pix_fmt yuvj420p
-level:v 4.1 -preset ultrafast -tune zerolatency \ -vcodec libx264 -r 10 -b:v
512k -s 640x360 \ -f mpegts -flush_packets 0
rtsp://192.168.1.4:5000?pkt_size=1316 
```

## Stream usb webcam

```bash ffmpeg -f v4l2 -framerate 25 -video_size 640x480 -i /dev/video0
output.mkv
```

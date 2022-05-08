# Webcam streaming

## Server

### Ultrafast

```sh
ffmpeg -i /dev/video0 -preset ultrafast -vcodec libx264 -b 900k -f mpegts udp://239.0.0.2:1234?pkt_size=1316
```

### Slow

## Client

```sh
ffplay udp://239.0.0.2
```

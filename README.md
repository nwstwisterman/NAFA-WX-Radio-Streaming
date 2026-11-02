# NAFA-WX-Radio-Streaming

North American Weather Radio Network is a weather radio streaming service affiliated with the North American Forecasters Association.

## Current station

- WXL20 — Rochester, NY — 162.550 MHz
- Public web server: https://nafa-wx-radio-streaming.onrender.com
- Render port: 10000
- HLS playlist: https://nafa-wx-radio-streaming.onrender.com/live/playlist.m3u8
- Live audio stream fallback: https://radio.nafawxradio.org/WXL20.mp3

## HLS browser streaming setup

This project is set up for browser-based streaming using HLS.

### Required source workflow

1. Use FFmpeg on a local machine with microphone input.
2. Generate HLS segments and a playlist file.
3. Upload the playlist and segment files to the Render app under a /live folder.
4. Point the browser player to the playlist URL.

### Example FFmpeg command

```bash
ffmpeg -f alsa -i default \
  -acodec libmp3lame -ar 44100 -b:a 128k \
  -f hls -hls_time 3 -hls_list_size 10 \
  -hls_segment_filename output/segment_%03d.ts \
  output/playlist.m3u8
```

### Browser player usage

```html
<audio controls>
  <source src="https://nafa-wx-radio-streaming.onrender.com/live/playlist.m3u8" type="application/x-mpegURL">
</audio>
```

This approach is intended for browser-only listeners and mic-based broadcasting.

WX Radio Streaming for all nations in the NAFA Coverage area (USA, Canada, Mexico)

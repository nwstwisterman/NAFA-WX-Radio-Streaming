# NAFA-WX-Radio-Streaming

North American Weather Radio Network is a weather radio streaming service affiliated with the North American Forecasters Association.

## Station

- WXL20 — Rochester, NY — 162.550 MHz
- Live stream: https://radio.nafawxradio.org/WXL20.mp3

## ShoutCast + BUTT setup

This station is designed to run as a ShoutCast stream so it can be fed live from the BUTT broadcasting tool.

Recommended BUTT settings for WXL20:

- Server: radio.nafawxradio.org
- Port: 8000
- Mount: /WXL20
- Login: source
- Password: your-shoutcast-source-password
- Format: MP3
- Bitrate: 128 kbps

Example source configuration:

- ShoutCast source URL: `http://radio.nafawxradio.org:8000`
- Mount point: `/WXL20`
- Source password: set in your ShoutCast source configuration

## Notes

- Update the source password in your ShoutCast server before going live.
- The public listener URL remains the stream URL above.
- Keep the station name and mount point aligned with your ShoutCast configuration so listeners can access the stream reliably.

WX Radio Streaming for all nations in the NAFA Coverage area (USA, Canada, Mexico)

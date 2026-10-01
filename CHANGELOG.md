## v21 (2026.10.01)

### Fixed
- "Source" quality now picks the highest resolution Twitch offers (for example 1440p). It used to take the first stream in Twitch's list, which stopped at 1080p when the 1440p stream is listed later.

## v20 (2026.10.01)

### New
- Forward proxy (HTTP or SOCKS5, with username and password) in Settings > AdBlock / Proxy. Changes apply immediately, no restart.
- "Test proxy with Twitch" checks the connection step by step: reaching the proxy, the tunnel, TLS and a real Twitch request.
- Source is the default video quality, and 1440p is requested from Twitch when the stream offers it.
- Stats for nerds shows the forward proxy in use, and the real video resolution instead of "-1 x -1".
- Auto-update works again. Update source can be changed in Settings > Application info > Updates.
- Changelog and About pages updated.

### Fixed
- "IOException - unexpected end of stream on null" with an authenticated proxy: the app now talks to a small local relay that adds the proxy login, so every part of the app (API, playlists, video) works with a proxy.
- Vaft and Video-Swap AdBlock now send your Twitch login, so 1440p is no longer capped at 1080p.
- "Install update" crashed the app on Android 14 and newer.
- Addresses on your own network (and the device itself) never go through the proxy.

### Notes
- Which qualities you get depends on Twitch and on where your proxy exits. A proxy in another country can hide 1440p.
- No proxy is configured by default. Enter yours in Settings > AdBlock / Proxy.

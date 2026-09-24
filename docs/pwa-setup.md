# PWA Setup (interim mobile client)

Until a native app exists, use the Progressive Web App approach.

## On the Jarvis host

1. Make sure Jarvis is running and its chat window is reachable on the LAN.
2. If it only binds to localhost, put a small reverse proxy (Caddy/nginx) in front that serves it on your LAN IP, port 80 or 443.
3. For HTTPS (needed for some iOS features), use a self-signed cert or Tailscale.

## On the iPad / iPhone

1. Open Safari → go to http://<jarvis-host-ip>/
2. Tap the Share icon → **Add to Home Screen**
3. Name it "Jarvis"
4. It now opens full-screen, no browser UI
5. Optional: enable Face ID / passcode on the device for extra security

## Voice

The phone/iPad mic can capture audio, but streaming it to the host Jarvis requires a small bridge (WebRTC or a simple websocket). For now, use text chat on the mobile device and keep voice on the desktop mic.

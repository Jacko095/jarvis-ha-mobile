# Jarvis HA Mobile

Companion project for running Jarvis as a chatbot + smart-home controller from your iPhone or iPad.

## Status

isair/jarvis has no native iOS app yet (upstream issue #17). This repo tracks the path to a proper mobile client and provides a working interim solution.

## Interim: PWA / web chat

While the desktop Jarvis app runs on your host machine, you can reach it from any phone or tablet on the same network:

1. Expose the Jarvis chat interface (or a lightweight proxy) on your LAN.
2. Open it in Safari on the iPad/iPhone.
3. Share → Add to Home Screen → it behaves like a native app.
4. Use text chat for questions and device control; voice works if the host mic is active.

## Target features (roadmap)

- [ ] Native SwiftUI / React Native client talking to Jarvis over a local API
- [ ] Voice input from the phone mic (streamed to host)
- [ ] Push notifications for HA events (doors, alarms, etc.)
- [ ] Offline-capable entity dashboard as fallback
- [ ] Biometric unlock for the wall panel

## Home Assistant integration

Same MCP setup as the wall-panel repo. See https://github.com/Jacko095/jarvis-home-assistant-wall

## Why two repos?

- `jarvis-home-assistant-wall` = the complete, ready-to-deploy kiosk setup (config + docs + scripts).
- `jarvis-ha-mobile` = the mobile client direction and interim PWA instructions.

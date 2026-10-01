# cozy

A browser-based cozy 3D hangout where small groups of friends walk around a cafe, forest or spaceship, sit together, and talk with spatial voice that sounds like it comes from each player's position.

> **Status:** early development. Phase 1 (a deployed spatial-voice room) is in progress.

## What makes it interesting

- **Sound through doorways.** Voices don't just get muffled by walls; they travel around corners and come out of the nearest doorway, using a portal graph and Web Audio.
- **Scaling past 12 players.** Interest management on the server (a spatial grid with distance-based update rates) and selective voice subscriptions keep per-player bandwidth flat as a room grows to 100+ players.
- **Join from a link.** No install, no account: open an invite link in a desktop browser and you're in.

## Stack

| Layer | Choice |
| --- | --- |
| Client | TypeScript, Vite, Three.js, Rapier (physics) |
| Game server | Go, WebSockets, 20 Hz authoritative tick |
| Voice | LiveKit (SFU) + Web Audio API spatialization |
| Hosting | Cloudflare Pages (client), Fly.io (server) |

## License

[MIT](LICENSE)

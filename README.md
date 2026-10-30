# Flagfire: Island Assault

A mobile-friendly three.js take on *Return Fire*: capture the enemy flag with a jeep while tanks, a helicopter and a mine-layer fight for the island's fuel and ammo.

- **Play:** https://flagfire.josephsammorris.workers.dev
- **Controls:** tap to move, hold FIRE to shoot (auto-aim), + / − to zoom, HANGAR at base to swap vehicles.

## Layout
- `public/index.html`: the whole game (HTML, CSS and JavaScript in one page)
- `wrangler.jsonc`: Cloudflare Workers config; `public/` is served as a static site

## Running locally
Any static file server works, e.g. `npx serve public`, or `npm run dev` for the Cloudflare dev server.

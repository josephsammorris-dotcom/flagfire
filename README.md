# Flagfire: Island Assault

A mobile-friendly three.js take on *Return Fire*: capture the enemy flag with a jeep while tanks, a helicopter and a mine-layer fight for the island's fuel and ammo.

- **Play:** https://flagfire.josephsammorris.workers.dev
- **Controls:** tap to move, hold FIRE to shoot (auto-aim), + / − to zoom, HANGAR at base to swap vehicles.

## Layout
- `public/index.html`: the whole game (HTML, CSS and JavaScript in one page)
- `public/vendor/three.module.min.js`: three.js r160, served locally (no CDN)
- `wrangler.jsonc`: Cloudflare Workers config; `public/` is served as a static site

## Graphics notes
- Scenery is merged into a few batches per map cell when the island is built (`bakeDecor`), and watchtowers,
  turret bases and parked vehicles are merged in place (`bakeModels`). Crushed trees lift themselves back out.
- Materials are shared through `M()` / `MT()`. Never edit a material from them in place; assign a different one.
- Quality steps down automatically on slow devices. Add `?fixedquality` to the URL to keep full quality.

## Running locally
Any static file server works, e.g. `npx serve public`, or `npm run dev` for the Cloudflare dev server.

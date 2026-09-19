# Synnical SVG

This repository publishes the Synnical SVG entry point.

The current `index.svg` loads the live Synnical OS deployment at `https://synnical.co.uk` inside an SVG/XHTML wrapper. This keeps the CDN entry point on Synnical and avoids shipping the old Cherri-derived static bundle.

CDN entry point:

- `https://cdn.jsdelivr.net/gh/synnical1/svg@main/index.svg`

For a true self-contained SVG build of the current Synnical frontend, the current Next.js client must be rebuilt specifically for static SVG delivery while continuing to use the live Synnical backend APIs/socket service.

# Synnical SVG

This repository publishes the full Synnical web build inside `index.svg`.

The SVG is a real XHTML `foreignObject` document that boots the bundled application code from this repository. It is not an image wrapper and it does not iframe `synnical.co.uk`.

CDN entry points:

- `https://cdn.jsdelivr.net/gh/synnical1/svg@latest/index.svg`
- `https://cdn.jsdelivr.net/gh/synnical1/svg@main/index.svg`

For an immutable build, replace `latest`/`main` with a commit SHA.

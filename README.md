# Synnical SVG

This repository publishes the Synnical SVG entry point.

## CDN entry point

- `https://cdn.jsdelivr.net/gh/synnical1/svg@main/index.svg`

## Rendering model

`index.svg` embeds the live Synnical OS deployment at `https://synnical.co.uk` inside an SVG/XHTML `foreignObject`.

The SVG deliberately has **no fixed pixel dimensions and no viewBox**. Chrome treats a directly opened SVG as an image document; giving it a 1366×768 intrinsic canvas causes the whole embedded UI to be fitted/resampled when the browser content area is a different size. That was the source of the visibly softer text, icons, borders and avatars in the CDN tab.

The root SVG, `foreignObject`, XHTML document and Synnical iframe now all stay at 100% of the actual browser viewport so the embedded site remains on the native CSS-pixel grid in windowed and fullscreen layouts.

The outer SVG also supplies the Synnical document title and the same Google Classroom tab icon used by the live Synnical deployment, so the CDN tab no longer falls back to jsDelivr's document identity.

Authentication, Chat, Socket.IO and Browser proxy traffic continue to use the live Synnical backend. No Synnical VPS deployment is performed by changes in this repository.

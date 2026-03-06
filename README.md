# colorthief-cli

CLI for extracting dominant colors and palettes from images.

This package bundles [colorthief](https://www.npmjs.com/package/colorthief) and
[sharp](https://www.npmjs.com/package/sharp) so the CLI works immediately via `npx`
with no extra setup.

## Quick start

```bash
npx colorthief-cli photo.jpg
npx colorthief-cli palette photo.jpg --count 5 --json
```

## Documentation

For full CLI documentation (all commands, flags, and output formats), see the
[Color Thief docs](https://lokeshdhakar.com/projects/color-thief/).

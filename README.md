# colorthief-cli

CLI for extracting dominant colors and palettes from images.

This package bundles [colorthief](https://www.npmjs.com/package/colorthief) and
[sharp](https://www.npmjs.com/package/sharp) so the CLI works immediately via `npx`
with no extra setup.

## Quick start

```bash
npx colorthief-cli photo.jpg
```

## Commands

```bash
# Dominant color
colorthief-cli photo.jpg

# Color palette
colorthief-cli palette photo.jpg

# Semantic swatches
colorthief-cli swatches photo.jpg
```

## Output formats

```bash
# Default: ANSI color swatches
colorthief-cli photo.jpg
# ▇▇ #e84393

# JSON with full color data
colorthief-cli photo.jpg --json

# CSS custom properties
colorthief-cli palette photo.jpg --css
# :root {
#     --color-1: #e84393;
#     --color-2: #6c5ce7;
# }
```

## Options

```bash
colorthief-cli palette photo.jpg --count 5        # Number of colors (2-20)
colorthief-cli photo.jpg --quality 1              # Sampling quality (1=best)
colorthief-cli photo.jpg --color-space rgb        # Color space (rgb or oklch)
```

Stdin is supported — use `-` or pipe directly:

```bash
cat photo.jpg | colorthief-cli -
```

Multiple files are supported. Output is prefixed with filenames, and `--json` wraps
results in an object keyed by filename.

> **Note:** If you already have `colorthief` and `sharp` installed in a project, you
> can also use `colorthief` directly as the command name (without the `-cli` suffix).

## Links

- [Color Thief docs & demo](https://lokeshdhakar.com/projects/color-thief/)
- [GitHub](https://github.com/lokesh/color-thief)

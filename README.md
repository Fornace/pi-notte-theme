# Notte

A near-black theme for the Pi coding agent.

## Palette

Open `preview.html` directly in a browser. The conversation and tool results are illustrative, not execution evidence.

| Role | Color |
|------|-------|
| Accent | `#7CC7FF` |
| Body text | `#DEE6F2` |
| Secondary text | `#9AA9BF` |
| Tool output | `#A6B8CE` |
| Pending tool background | `#000012` |
| Success tool background | `#001200` |
| Error tool background | `#120000` |
| User message background | `#00001A` |
| Custom message background | `#000010` |

Tool backgrounds use one RGB channel at 18/255. All other channels are zero. The canvas is black. Light blue replaces purple accents; secondary text has a cool tint.

This palette changes the original phosphor-green body text to soft blue-white. Green remains a success and diff signal.

## Pi compatibility

`notte.json` declares a dark appearance and all 56 current theme roles, including scrollbars, search highlights and `thinkingMax`.

Explicit hex values keep the palette independent of the terminal ANSI colors used by Pi's `system` theme.

## Install

Fornace installations receive this theme through `pi-fornace`, which installs and enforces `notte` on startup and updates. The source of truth is this repository; the distribution contains an exact copy.

For standalone Pi:

```sh
cp notte.json ~/.pi/agent/themes/notte.json
```

Select `notte` through `/settings`. Pi hot-reloads the active user theme when its file changes.

The preview includes left-hand tool rails. These require renderer integration in `pi-fornace`; theme JSON alone controls colors, not geometry.

## License

MIT. By Francesco Frapporti at [Fornace](https://fornace.it).

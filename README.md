# PSYCHRONIC_VideoOverlay

Allows video overlays on events with rotation, skew, transparency, optional audio, and optional dynamic scanlines using PIXI Video Textures.

## What It Does

This plugin enables video overlays on events using PIXI.js. It supports rotation, skew, transparency, optional audio, and an optional dynamically-generated scanline effect.

## Highlights

- The displayed video size is determined by the sprite's width/height, not the actual
- Audio playback is optional. If enabled, the video is unmuted and routed through the
- Smaller video display sizes reduce GPU overhead. For even better performance, provide
- If `scanlines` is true, a small 2x2 dynamic bitmap is created with a dark top row and

## Plugin Commands

- PlayVideoOverlay
- StopVideoOverlay

## Basic Usage

PlayVideoOverlay eventId:1 filename:"myvideo.mp4" sizeX:320 sizeY:240 scanlines:true

## Compatibility

- RPG Maker MZ
- JavaScript plugin for `js/plugins/`

## Installation

1. Download `PSYCHRONIC_VideoOverlay.js`.
2. Place it in your RPG Maker MZ project's `js/plugins/` folder.
3. Enable it from the RPG Maker Plugin Manager.

## Source

This version was exported from the RPG Reactor Complex template source plugin folder.

## Author

Psychronic

https://psychronic.itch.io

## License

MIT. See `LICENSE`.

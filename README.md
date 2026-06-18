# PSYCHRONIC_VideoOverlay

**RPG Maker MZ Plugin**

Allows video overlays on events with rotation, skew, transparency, optional audio, and optional dynamic scanlines using PIXI Video Textures.

## What It Does

This plugin enables video overlays on events using PIXI.js. It supports rotation, skew, transparency, optional audio, and an optional dynamically-generated scanline effect.

## Plugin File

- `PSYCHRONIC_VideoOverlay.js`
- Target: RPG Maker MZ
- Author: Psychronic
- URL: https://psychronic.itch.io

## Plugin Commands

- `PlayVideoOverlay`
- `StopVideoOverlay`

## Parameter Summary

- bufferDistance: The distance in pixels outside the screen within which videos start playing.
- debugMode: Print console logs for debugging. Disable for better performance.

## Installation

1. Download `PSYCHRONIC_VideoOverlay.js`.
2. Place it in your RPG Maker MZ project's `js/plugins/` folder.
3. Enable it from the RPG Maker Plugin Manager.
4. Configure any plugin parameters or commands listed below.

## Full Plugin Help

This plugin enables video overlays on events using PIXI.js. It supports rotation,
skew, transparency, optional audio, and an optional dynamically-generated scanline effect.

Videos are paused and hidden when off-screen, and reactivated when near the screen,
for performance reasons.

Key Notes:
- The displayed video size is determined by the sprite's width/height, not the actual
resolution of the video file. For best results, keep them proportional.
- Audio playback is optional. If enabled, the video is unmuted and routed through the
Web Audio API for in-game mixing.
- Smaller video display sizes reduce GPU overhead. For even better performance, provide
lower-resolution video files if needed.
- If `scanlines` is true, a small 2x2 dynamic bitmap is created with a dark top row and
transparent bottom row, tiled over the video to create a retro “CRT scanline” look.

Example usage with scanlines:
PlayVideoOverlay eventId:1 filename:"myvideo.mp4" sizeX:320 sizeY:240 scanlines:true

## Source

This standalone repository is generated from the latest PSYCHRONIC plugin source in the RPG Reactor Complex template.

## License

MIT. See `LICENSE`.

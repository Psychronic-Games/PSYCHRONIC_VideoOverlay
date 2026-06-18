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

### Play Video Overlay

- Command: `PlayVideoOverlay`
- Description: Adds a video overlay to a specified event with rotation, skew, transparency, and optional audio/scanlines.

Arguments:

- `eventId` (Event ID) - type: number; default: 1: The ID of the event to attach the video overlay to.
- `filename` (Filename) - type: string; default: myvideo.mp4: The filename of the video in /movies/ folder (e.g. myvideo.mp4).
- `sizeX` (Video Width) - type: number; default: 336: Width of the video in pixels.
- `sizeY` (Video Height) - type: number; default: 192: Height of the video in pixels.
- `xOffset` (X Offset) - type: number; default: 0: Horizontal offset from the event's center position.
- `yOffset` (Y Offset) - type: number; default: 0: Vertical offset from the event's center position.
- `zIndex` (Z-Index) - type: number; default: 1: Determines layering (higher values render above lower ones).
- `rotation` (Rotation) - type: number; default: 0: Rotation angle in degrees (0-360).
- `skewX` (Skew X) - type: number; default: 0: Skew angle along the X-axis in degrees.
- `skewY` (Skew Y) - type: number; default: 0: Skew angle along the Y-axis in degrees.
- `alpha` (Transparency) - type: number; default: 1.0: Transparency of the video overlay (0.0 to 1.0).
- `audio` (Audio) - type: boolean; default: false: Enable audio for the video overlay.
- `repeat` (Repeat) - type: boolean; default: true: Whether the video should loop. True by default.
- `scanlines` (Scanlines) - type: boolean; default: false: Whether to overlay a retro scanline effect on the video.

### Stop Video Overlay

- Command: `StopVideoOverlay`
- Description: Removes a video overlay from a specified event.

Arguments:

- `eventId` (Event ID) - type: number; default: 1: The ID of the event to remove the video overlay from.

## Parameter Summary

- bufferDistance: The distance in pixels outside the screen within which videos start playing.
- debugMode: The ID of the event to remove the video overlay from.

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

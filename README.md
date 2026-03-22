# SquishIt — Releases

Power-user desktop media compression for Windows.  
Modern codecs (AV1, HEVC, H.264) · Hardware acceleration · Explorer right-click integration

---

## ⬇ Latest Download

**[SquishIt-Setup-v1.2.1.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.2.1/SquishIt-Setup-v1.2.1.exe)** &nbsp;·&nbsp; v1.2.1 &nbsp;·&nbsp; Released 2026-03-22

> ## What's New  
> - Quick Compress no longer starts immediately. It now waits for an explicit Start Compression click so you can actually choose Lite, Balanced, or Max every time.  
> - Quick Compress stays open after finishing instead of disappearing on its own.  
> ## Fixes

---

## All Releases

| Version | Released | Download |
|---------|----------|----------|
| **v1.2.1** | 2026-03-22 | [SquishIt-Setup-v1.2.1.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.2.1/SquishIt-Setup-v1.2.1.exe) |
| **v1.2.0** | 2026-03-22 | [SquishIt-Setup-v1.2.0.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.2.0/SquishIt-Setup-v1.2.0.exe) |

---

## Release Notes

### v1.2.1 — 2026-03-22

## What's New

- Quick Compress no longer starts immediately. It now waits for an explicit Start Compression click so you can actually choose Lite, Balanced, or Max every time.
- Quick Compress stays open after finishing instead of disappearing on its own.

## Fixes

- Fixed Max preset failures on builds where the bundled FFmpeg does not include SVT-AV1. Codec availability is now detected against the bundled FFmpeg binary instead of a different system FFmpeg on PATH.
- When Max is not available in the bundled build, Quick Compress now clearly tells you and falls back to the best available codec for that build.
- Output preview stays aligned with the real codec/container choice for the selected preset.

### v1.2.0 — 2026-03-22

* Release


*

---

## System Requirements

- Windows 10 / 11 (64-bit)
- ~50 MB disk space
- No additional runtime or dependencies required

## Installation

1. Download the setup installer above.
2. Run it — no elevated privileges required for a per-user install.
3. During setup, optionally enable the Explorer right-click context menu.

---

*This repository contains only release builds. Source code is private.*

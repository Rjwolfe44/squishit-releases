# SquishIt — Releases

Power-user desktop media compression for Windows.  
Modern codecs (AV1, HEVC, H.264) · Hardware acceleration · Explorer right-click integration

---

## ⬇ Latest Download

**[SquishIt-Setup-v1.2.0.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.2.0/SquishIt-Setup-v1.2.0.exe)** &nbsp;·&nbsp; v1.2.0 &nbsp;·&nbsp; Released 2026-03-22

> **Quick Compress preset selector** — choose Lite, Balanced, or Max right from the right-click window.  
> **Auto-update** — the app checks for new releases on startup and shows a one-click install banner.

---

## All Releases

| Version | Released | Download |
|---------|----------|----------|
| **v1.2.0** | 2026-03-22 | [SquishIt-Setup-v1.2.0.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.2.0/SquishIt-Setup-v1.2.0.exe) |

---

## Release Notes

### v1.2.0 — 2026-03-22

## What's New

- **Quick Compress preset selector** — Lite (H.264 fast), Balanced (HEVC), and Max (SVT-AV1) presets are now selectable directly in the right-click compression window. Your last choice is remembered.
- **Auto-update system** — SquishIt now checks for new releases on startup (once per 24 h). When an update is found, a banner appears with a one-click "Download & Install" button that streams the new installer and applies it silently.

## Bug Fixes & Improvements

- Fixed AV1 Max mode crash (`-svtav1-params` option unsupported by bundled FFmpeg — removed).
- Fixed "Open in SquishIt" spawning a duplicate window when the app is already running (single-instance IPC via local TCP).
- Compress / Clear buttons no longer get cut off when resizing the window.
- Startup is significantly faster — hardware detection and compressor creation are deferred to background threads.

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

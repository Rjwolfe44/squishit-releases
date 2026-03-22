# SquishIt — Releases

Power-user desktop media compression for Windows.  
Modern codecs (AV1, HEVC, H.264) · Hardware acceleration · Explorer right-click integration

---

## ⬇ Latest Download

**[SquishIt-Setup-v1.3.1.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.3.1/SquishIt-Setup-v1.3.1.exe)** &nbsp;·&nbsp; v1.3.1 &nbsp;·&nbsp; Released 2026-03-22

> ## What's New  
> - Doubled the main window base size for the full app and clamp it safely to the current display so the larger default layout opens reliably on real screens.  
> - Added manual update checks from the About dialog.  
> - Added a History button and history window for completed compression jobs, with clear-history support and saved-space totals.

---

## All Releases

| Version | Released | Download |
|---------|----------|----------|
| **v1.3.1** | 2026-03-22 | [SquishIt-Setup-v1.3.1.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.3.1/SquishIt-Setup-v1.3.1.exe) |
| **v1.2.2** | 2026-03-22 | [SquishIt-Setup-v1.2.2.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.2.2/SquishIt-Setup-v1.2.2.exe) |
| **v1.2.1** | 2026-03-22 | [SquishIt-Setup-v1.2.1.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.2.1/SquishIt-Setup-v1.2.1.exe) |
| **v1.2.0** | 2026-03-22 | [SquishIt-Setup-v1.2.0.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.2.0/SquishIt-Setup-v1.2.0.exe) |

---

## Release Notes

### v1.3.1 — 2026-03-22

## What's New

- Doubled the main window base size for the full app and clamp it safely to the current display so the larger default layout opens reliably on real screens.
- Added manual update checks from the About dialog.
- Added a History button and history window for completed compression jobs, with clear-history support and saved-space totals.
- Added a profile editor dialog for creating, duplicating, editing, and deleting custom profiles.
- Added configurable output filename templates with tokens for file name, profile, codec, CRF, date, and timestamp.
- Added parallel compression with a configurable job limit.
- Added Windows completion notifications.
- Added right-click actions on queued files, including compress-this-file, move-to-top, copy-path, and open-location actions.

## Reliability Fixes

- Fixed a startup crash caused by the history manager constructor mismatch.
- Fixed history persistence so completed jobs are actually written and shown in the new history UI.
- Fixed AV1 software encoding on bundled FFmpeg builds by correcting libaom-av1 preset mapping to the real supported cpu-used range.
- Added a safer AV1 retry path when FFmpeg rejects an initial software AV1 option set.
- Fixed queue reordering so Move to Top affects actual processing order, not just the visible card layout.

## Packaging

- Installer pipeline now produces installer-only output.
- Published as v1.3.1 for the first public 1.3.x release after v1.2.2.

### v1.2.2 — 2026-03-22

## What's New

- Quick Compress still waits for an explicit Start Compression click so preset choice stays intentional.
- After a successful quick compression, the window now closes automatically again.

## Fixes

- Restored the original auto-close behavior after success without bringing back the old auto-start regression.
- Failure cases still stay open so the error message can be read and retried.

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

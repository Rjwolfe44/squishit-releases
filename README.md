# SquishIt — Releases

Power-user desktop media compression for Windows.  
Modern codecs (AV1, HEVC, H.264) · Hardware acceleration · Explorer right-click integration

---

## ⬇ Latest Download

**[SquishIt-Setup-v1.5.1.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.5.1/SquishIt-Setup-v1.5.1.exe)** &nbsp;·&nbsp; v1.5.1 &nbsp;·&nbsp; Released 2026-04-01

> ## What changed  
> - Added a real auto target-size mode that resolves per source file into fast, balanced, or strict instead of behaving like a static label.  
> - Made auto resource use and auto thread selection workload-aware so heavy software AV1, hardware encodes, and multi-job runs choose more sensible budgets.  
> - Fixed the GUI batch path so auto thread selection is decided by the compressor at encode time instead of being frozen too early in the window layer.

---

## All Releases

| Version | Released | Download |
|---------|----------|----------|
| **v1.5.1** | 2026-04-01 | [SquishIt-Setup-v1.5.1.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.5.1/SquishIt-Setup-v1.5.1.exe) |
| **v1.5.0** | 2026-04-01 | [SquishIt-Setup-v1.5.0.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.5.0/SquishIt-Setup-v1.5.0.exe) |
| **v1.4.0** | 2026-03-23 | [SquishIt-Setup-v1.4.0.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.4.0/SquishIt-Setup-v1.4.0.exe) |
| **v1.3.1** | 2026-03-22 | [SquishIt-Setup-v1.3.1.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.3.1/SquishIt-Setup-v1.3.1.exe) |
| **v1.2.2** | 2026-03-22 | [SquishIt-Setup-v1.2.2.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.2.2/SquishIt-Setup-v1.2.2.exe) |
| **v1.2.1** | 2026-03-22 | [SquishIt-Setup-v1.2.1.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.2.1/SquishIt-Setup-v1.2.1.exe) |
| **v1.2.0** | 2026-03-22 | [SquishIt-Setup-v1.2.0.exe](https://github.com/Rjwolfe44/squishit-releases/releases/download/v1.2.0/SquishIt-Setup-v1.2.0.exe) |

---

## Release Notes

### v1.5.1 — 2026-04-01

## What changed
- Added a real auto target-size mode that resolves per source file into fast, balanced, or strict instead of behaving like a static label.
- Made auto resource use and auto thread selection workload-aware so heavy software AV1, hardware encodes, and multi-job runs choose more sensible budgets.
- Fixed the GUI batch path so auto thread selection is decided by the compressor at encode time instead of being frozen too early in the window layer.
- Updated the live encoder preview to show the resolved auto governor and target-size behavior more clearly.

## Validation
- Full test suite passed before release.

### v1.5.0 — 2026-04-01

## What's New

- Added fast, balanced, and strict target-size modes with iterative bitrate convergence for closer MB matching.
- Added preflight skipping when the requested target is not smaller than the source file.
- Added sample compare mode for quick codec checks and new batch queue-order controls.
- Added resource-governor controls for safer thread budgeting and multi-job behavior.

## Compression Improvements

- Retuned AV1 defaults to prefer faster practical paths.
- Improved AMD AV1 hardware quality mode by switching to a saner QVBR-based path.
- Kept the keep-original safeguard while making target-size retries and warnings more explicit.

## Release Hardening

- Added version-alignment checks across app, package, and installer metadata before publishing.
- Expanded automated coverage for target-size planning, CLI flags, and compare-mode surfaces.

### v1.4.0 — 2026-03-23

﻿## What's new
- Added a live encoder/thread preview in the main window.
- Dynamic codec filtering now hides unavailable encoders and reflects real GPU support.
- Strong/Extreme AV1 now favors compression efficiency and retries with stronger settings when needed.
- Multicore tuning was improved for AV1, SVT-AV1, and VP9.
- Cancel now stops active jobs without showing a fake completion toast.

## Fixes
- Better progress tracking using encoded timestamps and frame counts from ffprobe.
- More accurate CPU/GPU reporting in the UI.
- Installer rebuilt with the latest release polish.

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

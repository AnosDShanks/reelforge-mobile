# REELFORGE Mobile V1.1

Free, static, mobile-first creator studio. No paid APIs or server.

## Installation / updating GitHub Pages
Upload all five files (`index.html`, `sw.js`, `manifest.webmanifest`, `icon.svg`, `README.md`) **individually** into the **root** of your existing public `reelforge-mobile` repository, replacing the old versions. Commit to `main`. Keep Settings → Pages set to `Deploy from a branch`, `main`, `/(root)`. Open your GitHub Pages URL in Safari and reload; if the old version persists, close and reopen the Home Screen app or clear website data after exporting project backups.

## V1.1 features
- Template-based script drafting, scene editing, storyboard preview, device speech playback, local project saves, JSON/TXT export/import.
- Add your own photos to individual scenes (compressed on device).
- Export a PNG image of the selected scene.
- **Experimental** silent vertical video export through browser `canvas.captureStream` + `MediaRecorder`, with file format selected from actual browser support. Some iPhones/Safari versions cannot record a canvas stream, or may produce WEBM instead of MP4. No guarantee of MP4 on iPhone. Video output has **no narration audio**, even if speech playback works. Rendering runs in real time; keep the screen active.
- Export size choices 540×960, 720×1280, 1080×1920; start at 540p.

## Limitations and data safety
Projects live in browser localStorage and can disappear when browser data is cleared. Uploaded images are embedded as compressed data URLs in project JSON, so storage limits may be reached; use Export JSON for backup. Public GitHub repositories must not contain private client files. No AI models, automatic image retrieval, background jobs, cloud rendering, music, captions synchronized to words, or publishing integrations.

## Later Windows/HP migration
Export JSON with fields `version`, `topic`, `niche`, `duration`, `style`, `script`, `projectName`, `scenes` (`heading`, `caption`, optional `image` data URL). A future Python/FastAPI + FFmpeg backend can consume the same JSON and provide proper MP4, voiceovers and batch processing.

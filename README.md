# REELFORGE Mobile V1

A free, static, mobile-first creator workspace. No paid API, backend, or account required.

## Features that actually work
- Template-based (not AI) narration draft based on topic and category
- Editable script and storyboard scenes
- Timed vertical storyboard preview with four color themes
- iPhone browser text-to-speech playback (availability depends on browser/device)
- Save/load projects in browser localStorage
- Export script TXT and portable project JSON; import JSON
- Offline cache after first successful visit on HTTPS (service worker)

## Not included yet
- Generative AI scripts, generated images, speech audio files, automatic captions from audio, MP4 video rendering, or automatic social publishing.
- The storyboard is NOT a downloadable video. Free stock footage is not automatically fetched.

## Publish for free using GitHub Pages
1. Create a free GitHub account and a public repository named `reelforge-mobile`.
2. Upload the **contents** of this folder (index.html, manifest.webmanifest, icon.svg, sw.js) to the repository root.
3. In repository Settings → Pages, choose **Deploy from a branch**, branch **main**, folder **/(root)**, and save.
4. Wait for GitHub Pages to show the live HTTPS address, usually `https://YOUR_USERNAME.github.io/reelforge-mobile/`.
5. Open that live address in Safari on iPhone. Tap Share → Add to Home Screen → Add.
6. Create a test project and use Export project JSON as a backup.

GitHub Pages requires a public repository on GitHub Free. Do not upload private information or client assets to a public repository. The app itself keeps saved projects locally on the device, not in the repository.

## Later Windows/HP migration
The portable JSON project schema includes `version`, `topic`, `niche`, `duration`, `style`, `script`, `projectName`, and `scenes` with `heading`/`caption`. A future Python/FastAPI + FFmpeg worker can ingest exported JSON without changing the mobile UI design. Local generation can be connected later over an authenticated HTTPS API.

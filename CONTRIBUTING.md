# Contributing to Caption Saathi

Help creators fix subtitle problems on phones and computers.

## Report a problem
Open an issue with your device, browser, steps to reproduce, expected result, and actual result. Include a small fictional SRT example if useful. Do not upload private subtitles, videos, credentials, or personal information.

## Make a change
1. Fork this repository and create a branch.
2. Serve the `dist` folder with a static HTTP server. For example, with Python installed: `python -m http.server 8000 --directory dist`.
3. Keep subtitle and video processing on the device. Do not add trackers or remote file uploads.
4. Check imports, editing, timing adjustments, undo, and export. Include a small regression example for parser or timing fixes.
5. Open a pull request describing the problem, change, and checks performed.

The interface uses plain HTML, CSS, and JavaScript. There is no dependency installation or build step. `dist/core.js` contains subtitle parsing and formatting; `dist/app.js` contains interface behavior.

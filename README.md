# Caption Saathi
A browser-only SRT editor for Hindi, Hinglish and English creators. No backend or paid API. Files remain on the device.

## Use
Serve `dist/` with any static HTTP server. Open the site, load an SRT file (or try the sample), adjust timing, edit captions, and download an SRT. A local video can optionally be selected for synchronized preview.

## Features
- Strict SRT parsing with clear errors rather than silent skipped captions
- Timing shift with negative timestamp protection
- Editable timestamps and text; undo history
- Grapheme-aware line wrapping where Intl.Segmenter is supported
- Overlap, ordering, short-duration, empty-text, and line-length checks
- Local video preview and SRT export

## Limits
No speech transcription, translation, AI video generation or burned-in video export. Reflow preserves words and timestamps; captions needing more than two lines need manual editing. Files are not persisted after closing. Large subtitle files may be slow on phones. Browser video codec support varies. Subtitle formatting tags are treated as literal text in the preview.

## Contributing
Describe the problem and reproduction steps in an issue. For code changes, keep file processing local and include a small example SRT demonstrating any parser or timing fix. Never include private footage or personal subtitle files.

## Run locally
With Python installed, run `python -m http.server 8000 --directory dist`, then open `http://localhost:8000`. No package installation or build step is required. Serve the files over HTTP rather than opening `index.html` directly, because the app uses JavaScript modules.

## Hosting
Deploy the contents of `dist/` to a static website host. A public demo is not configured in this repository yet.

## Project status
Early working prototype. The creator has tested the initial website on a phone. Import/export round-trip, overlap detection, short-duration detection, invalid input rejection, and line wrapping have received basic automated checks. Wider device and accessibility testing are welcome. This project was developed with AI assistance.

## License
MIT. See [LICENSE](LICENSE). Contribution guidance is in [CONTRIBUTING.md](CONTRIBUTING.md).

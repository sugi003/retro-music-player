Retro Tamil Music Player
=========================

Quick start
-----------
1. Open `retro-player.html` in your browser (double-click or use a local web server).

2. The player comes with a small demo playlist and a gallery. Local demo files were downloaded to:
   - `images/sample1.jpg`
   - `images/sample2.jpg`
   - `audio/sample1.mp3`

3. To use your own Tamil songs:
   - Place MP3 files under `audio/`.
   - Edit the `tracks` array inside `retro-player.html` and set each track's `file` to the relative path (e.g. `audio/my-song.mp3`).
   - Set `lang: "ta"` for Tamil tracks if you want to filter by the Language selector.

Gallery
-------
- The gallery prefers local images in `images/` (e.g. `images/sample1.jpg`, `images/*.jpg`).
- If local images aren't found, it uses online placeholders.

Editing / Adding tracks example
------------------------------
Inside `retro-player.html` you'll find the `tracks` array near the top of the script. Each item looks like:

{ title: "Song Title", artist: "Artist Name", file: "audio/filename.mp3", length: "03:30", lang: "ta" }

- `file` must point to a relative path (if using local audio) or an absolute URL.
- `length` is a display-only field; the player reads actual duration from the audio file when available.

Local server (optional)
-----------------------
For more consistent behavior (CORS, media loading) run a simple local server in this directory:

PowerShell:

```powershell
cd "d:\retro music player"
python -m http.server 8000
# then open http://localhost:8000/retro-player.html
```

(Or use `npx http-server` / other local server tools.)

Notes
-----
- The language selector filters tracks by the `lang` field. Choose `All` to see every track.
- Replace placeholder images and audio with your own to fully customize the player.

If you'd like, I can:
- Add a small script to auto-generate the `tracks` array from an `audio/manifest.json` you place in the folder.
- Add drag-and-drop upload UI (requires running a small local server to actually store files).

Enjoy — tell me which next step you'd like me to take (manifest, drag-and-drop UI, or more playlist additions).
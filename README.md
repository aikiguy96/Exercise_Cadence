# Exercise Cadence

A compact exercise-tempo coach that works in a browser and can be hosted on **GitHub Pages**. No backend, libraries, build process, or internet connection required after the page loads.

## Features

- 1–999 repetitions
- Eccentric and concentric motion times (0.2–120 seconds)
- Independent **top and bottom pauses** (0–120 seconds; 0 skips the hold)
- Configurable **pre-set countdown** (0–60 seconds)
- Choose **eccentric-first** (start at TOP) or **concentric-first** (start at BOTTOM)
- Animated TOP ↔ BOTTOM position marker and phase time remaining
- Optional high-pitched TOP and low-pitched BOTTOM arrival tones
- Start, Pause/Resume, Reset and elapsed exercise time
- Responsive dark layout, screen-wake attempt on supported devices
- Auto-pause when the browser tab becomes hidden

## Exercise timing

An eccentric-first rep has this sequence:

1. TOP → BOTTOM: eccentric movement
2. BOTTOM: optional bottom pause
3. BOTTOM → TOP: concentric movement
4. TOP: optional top pause

A concentric-first rep has this sequence:

1. BOTTOM → TOP: concentric movement
2. TOP: optional top pause
3. TOP → BOTTOM: eccentric movement
4. BOTTOM: optional bottom pause

Every repetition includes the relevant endpoint pauses, **including the final repetition**. If a hold is set to zero, the following movement begins immediately. The countdown occurs before the first movement and is **not** included in elapsed exercise time. Tones sound upon reaching the endpoints, including the initial starting position; they do not sound again when a hold ends. The repetition counter advances after a full cycle, including its final hold.

Example: 10 repetitions × (3 s eccentric + 1 s bottom pause + 2 s concentric + 1 s top pause) = **70 seconds of exercise**, plus any starting countdown.

## Publish on GitHub Pages

1. Create a public GitHub repository (e.g., `exercise-cadence`).
2. Upload the included `index.html`, `README.md`, and `LICENSE` files into the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Choose `main` and `/(root)`, then **Save**.
6. Visit `https://YOUR-USERNAME.github.io/exercise-cadence/` after deployment.

## Run locally

Open `index.html` directly, or serve the folder with:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000/.

## Notes

- Audio may require a tap/click on Start; device volume and browser silent-mode behavior vary.
- If the browser tab is hidden or the screen locks, playback pauses rather than silently skipping repetitions.
- Browser audio/animation timing is best-effort, not precision or medical instrumentation.
- No workout data, settings, history, or personal information is saved.
- The timer engine separates per-set cadence settings from playback state, making it suitable for a future exercise routine/prescription layer.

## Files

- `index.html`: complete app (HTML/CSS/JavaScript)
- `README.md`: instructions
- `LICENSE`: MIT License

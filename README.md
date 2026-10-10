# Exercise Cadence

A small, mobile-friendly exercise tempo coach. Runs entirely in your browser and is ready for free hosting with **GitHub Pages**. No dependencies, build tools, accounts, or backend needed.

## Features

- Adjustable repetitions (1–999)
- Independent eccentric and concentric phase durations (0.2–120 seconds each)
- Animated TOP ↔ BOTTOM marker, current phase, rep count, and remaining phase time
- Distinct high (top) and low (bottom) audio cues (optional)
- Start, Pause/Resume, Reset
- Dark theme and responsive display
- Attempts to keep the screen awake during a set on supported browsers
- Automatically pauses if the tab is hidden to avoid running a workout unnoticed

## Publish on GitHub Pages

1. Create a public GitHub repository (for example, `exercise-cadence`).
2. Upload `index.html` and `README.md` to the repository's root directory, or commit and push using Git.
3. Open **Settings → Pages** in the GitHub repository.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select branch **main**, folder **/(root)**, then **Save**.
6. When deployment completes, open `https://YOUR-USERNAME.github.io/exercise-cadence/` (substitute your username/repository name).

## Run locally

Open `index.html` directly in a modern browser, or use a simple web server:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000/`.

## Usage

Set **Repetitions**, **Eccentric (s)**, and **Concentric (s)**. Enable or disable audible cues. Press **Start**. The first cue marks **TOP**. The marker descends during the eccentric phase; a lower cue marks **BOTTOM**; it then ascends during the concentric phase. At TOP it sounds the high cue and the next repetition begins, until the set ends.

Example: 10 reps × (3 s eccentric + 2 s concentric) = 50 s of movement.

## Notes

- On many browsers, sound must be initiated by a user action such as pressing Start. Check device volume and silent-mode restrictions.
- Keep the app visible for continuous timing. When you change tabs or lock the screen, the app pauses as a safety-oriented behavior.
- Browser animation and audio are best-effort cues, not medically accurate measurement or real-time control.
- A repetition is counted after **both** eccentric and concentric phases complete.
- The program does not store personal data, exercise logs, or preferences.

## Project files

- `index.html` — complete app (HTML, CSS, JavaScript)
- `README.md` — setup and usage guide
- `LICENSE` — MIT license

## License

MIT.

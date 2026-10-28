# AIMLABS WEB - Cyber Aim Trainer

A browser-based 3D aim trainer with four short practice scenarios, configurable mouse sensitivity and crosshair, session summaries, and a local leaderboard.

## Get started

### Option 1: Open the page directly

Open `index.html` in a recent desktop browser. An internet connection is needed to load the page's CDN-hosted libraries, fonts, and icons.

### Option 2: Run a local web server

From the project folder in PowerShell, start Python's built-in web server:

```powershell
py -m http.server 8000
```

If `py` is not available but Python is installed, use:

```powershell
python -m http.server 8000
```

Then open <http://localhost:8000/>. The server serves `index.html` as the home page. Stop the server with `Ctrl+C`.

No build step or package installation is required. Keep the HTML, CSS, and JavaScript files together in the project folder so the page can load its local assets.

## Start a training session

1. Open the **TRAIN** tab and choose a scenario.
2. The browser will capture the mouse pointer so you can aim around the 3D arena.
3. Aim with the mouse and click the **left mouse button** to shoot. In Sphere Track, keep clicking the moving target to drain its health.
4. Each task lasts 60 seconds. When the timer ends, review your score, accuracy, kills per second, reaction time, and hit heatmap.
5. Choose **REPLAY TASK** to run that scenario again or **MAIN MENU** to choose another.
6. Press **Esc** to end the current task, release the pointer, and open the results summary.

Use the **SETTINGS** tab before starting to adjust sensitivity, field of view, target color, crosshair, and audio volume. To compare sessions, keep your sensitivity and field of view consistent.

## Training scenarios

| Scenario | Focus | What to practice |
| --- | --- | --- |
| Gridshot | Flicking | Acquire and hit three targets that remain on screen. |
| Microflex | Precision | Make small, controlled adjustments to hit smaller targets. |
| Sphere Track | Tracking | Follow the moving target and land repeated shots. |
| Reflex | Reaction | Acquire and hit the single target quickly. |

## Scores and saved data

The post-session leaderboard stores up to 20 score records in this browser's local storage. Records are local to the browser profile and are not uploaded to a server. Use **LEADERBOARD** to view them or **RESET HISTORY** to clear them. Clearing browser site data also removes the records.

## Project files

- `index.html` — page structure and game engine.
- `styles.css` — custom page styling.
- `audio.js` — synthesized hit, miss, and tracking sounds.

The page also loads Tailwind CSS, Three.js, Google Fonts, and Font Awesome from external CDNs.

## Troubleshooting

- **The page looks unstyled or icons/fonts are missing:** check your internet connection; those resources are loaded from CDNs.
- **The mouse does not control aiming:** click a training scenario and allow the browser to lock the pointer. Press `Esc` to release it.
- **The 3D arena does not appear:** use a modern desktop browser with WebGL enabled and up-to-date graphics drivers.
- **Scores are missing:** the leaderboard is specific to the browser profile and device where each session was played.

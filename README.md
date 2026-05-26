# KeyCoach Research Pro

**Science-based touch typing coach with adaptive drills, spaced review, replay analytics, and a fully local/offline-first design.**

KeyCoach Research Pro is a standalone browser app for improving typing speed, accuracy, rhythm, and transfer to real writing. It combines short structured practice sessions with adaptive weak-target drills, heatmaps, session replay, local progress tracking, and a research-inspired coaching layer.

The app is designed to run from a single HTML file with no required backend, account, database, or cloud service.

---

## Highlights

- **Single-file app** — open the HTML file directly in a browser.
- **Offline-first** — core training data stays in browser storage.
- **Science-based training flow** — warm-up, focused drills, interleaved review, and transfer practice.
- **Adaptive coaching** — adjusts target pace, difficulty, hint policy, and correction style from local performance.
- **Weak-target drills** — identifies weaker keys and bigrams, then generates focused practice.
- **Live typing metrics** — WPM, accuracy, consistency, hints, progress, ETA, and phase time.
- **Keyboard heatmap** — visualises errors, hesitation, and finger-level performance.
- **Session replay** — scrub and replay previous typing attempts.
- **Custom drill lab** — paste or generate a prompt, type it, score it, and save results locally.
- **Research coach reports** — generate or download a markdown report with recommendations.
- **PWA helpers** — built-in manifest support and downloadable `sw.js` / `manifest.json` helpers.
- **Privacy focused** — no network calls required; export/import data as JSON.
- **Accessibility upgrades** — keyboard-friendly UI, high-focus mode, reduced-motion support, and mobile capture improvements.

---

## Demo / App Structure

KeyCoach is organised into three main areas:

### Practice

The daily session runner lets users choose:

- Text mode: **Office**, **Student**, or **Programmer**
- Session length: **6, 10, or 15 minutes**
- Target WPM
- Training plan: **Auto**, **Bigrams**, **Keys**, **Mixed**, or **Transfer AI**
- AI difficulty

Practice sessions use short phases:

1. Warm-up
2. Focused drills
3. Interleaved review
4. Transfer text

The coach tracks typing speed, accuracy, consistency, hints, progress, and time remaining while giving immediate feedback.

### Insights

The Insights area includes:

- Keyboard heatmap
- Error view
- Hesitation view
- Finger summary
- Weak targets
- Progress chart
- Top confusions
- Session replay with speed controls

### Settings

The Settings area includes:

- Hint policy
- Correction mode
- Rhythm mode
- Rhythm sound
- Export data
- Import data
- Reset all data
- PWA helper tools
- Research Lab for custom drills, reports, accessibility toggles, and microbreak nudges

---

## Research-Inspired Learning Model

KeyCoach Research Pro is built around practical learning principles:

### Spaced Review

Keys and bigrams become due for review over time. Stronger items are shown less often, while weaker items return sooner.

### Retrieval Practice

The app encourages the user to type from memory rather than relying on constant visual hints. Hints can be faded as accuracy improves.

### Interleaving

Instead of repeating only one easy pattern, the coach mixes weak transitions with realistic text so the skill transfers better to real typing.

### Desirable Difficulty

The app can raise or lower the target pace and AI difficulty depending on recent accuracy. This keeps sessions challenging without turning them into speed-only practice.

### Immediate Feedback

Errors are marked during typing, and the replay/heatmap systems make it easier to review what happened after a session.

### Transfer Practice

Transfer checks and realistic text modes help measure whether improvements carry over beyond isolated drills.

---

## Research Upgrade Layer

The v3 research layer adds extra tools while preserving the original app structure.

### Adaptive Defaults

Click **Apply adaptive defaults** to update:

- Target WPM
- AI difficulty
- Hint policy
- Correction mode
- Rhythm default

The recommendation is based on recent local session data.

### Weak-Target Drill Builder

Click **Build weak-target drill** to generate a custom prompt from weak keys and bigrams found in local typing stats.

### Custom Drill Scoring

In the Research Lab:

1. Enter or generate a prompt.
2. Type the prompt in the response box.
3. Click **Save custom drill result**.
4. The result is saved into local KeyCoach stats.

### Research Coach Report

The report includes:

- Session count
- Replay count
- Recent WPM / accuracy trend
- Last session summary
- Recommended next session
- Weak keys
- Weak bigrams
- Research-inspired guidance

Use **Show research report** or **Download report**.

### Microbreak Nudges

Optional microbreak nudges encourage short pauses when performance suggests fatigue or loss of rhythm.

### High-Focus Accessibility

High-focus mode strengthens focus outlines and cursor visibility, making keyboard navigation clearer.

---

## Getting Started

### Option 1: Run Directly

1. Download the HTML file.
2. Open it in a modern browser.
3. Start a session.

No build step is required.

### Option 2: Run with a Local Server

Using a local server is recommended if you want PWA behaviour to work more reliably.

```bash
python -m http.server 8080
```

Then open:

```text
http://localhost:8080
```

---

## PWA Setup

The app includes PWA helper buttons for downloading:

- `manifest.json`
- `sw.js`

For full installability:

1. Put the HTML file, `manifest.json`, and `sw.js` in the same folder.
2. Serve the folder from `localhost` or HTTPS.
3. Open the app in the browser.
4. Use the browser install prompt if available.

---

## Data and Privacy

KeyCoach stores data locally in the browser using `localStorage`.

Stored data may include:

- Profile settings
- Typing sessions
- Per-key stats
- Per-bigram stats
- Finger stats
- Confusion data
- Replay data
- Research upgrade settings
- Custom drill prompts and scores

The app is designed so training can happen without sending typing data to a server.

### Export Data

Use **Settings → Export data** to download a JSON backup.

### Import Data

Use **Settings → Import data** to restore a previous JSON export.

### Reset Data

Use **Settings → Reset ALL data** to clear all stored progress.

---

## Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Esc` | Pause session |
| `?` | Show keyboard peek |
| `Alt + R` | Open / refresh research report |

---

## Training Modes

| Mode | Best for |
|---|---|
| Office | Emails, messages, admin writing, documents |
| Student | Essays, explanations, paragraphs, academic-style writing |
| Programmer | Symbols, snippets, brackets, punctuation, and code-like patterns |

---

## Correction Modes

| Mode | Description |
|---|---|
| Flow | Keep moving; avoid over-fixing while drilling |
| Realistic | Allow backspace and normal correction behaviour |
| Strict | Prioritise accuracy and correction before moving on |

---

## Suggested Practice Routine

For most users:

1. Start with a 6- or 10-minute Auto session.
2. Keep accuracy above speed.
3. Check Insights after the session.
4. Use weak-target drills for the weakest bigrams or keys.
5. Run a transfer check.
6. Export data occasionally as a backup.

---

## Project Goals

KeyCoach Research Pro aims to be:

- Fast to open
- Useful offline
- Private by default
- Good for short daily practice
- More intelligent than basic typing tests
- Focused on transfer to real writing
- Friendly to learners who need clearer feedback and less visual noise

---

## Roadmap Ideas

Future improvements could include:

- Optional multiple keyboard layouts
- Left/right hand balance charts
- More detailed fatigue detection
- Custom lesson packs
- Teacher/classroom export format
- CSV export for sessions
- More advanced replay timeline analytics
- Optional cloud sync, kept separate from the local-first core
- Better mobile-specific typing exercises
- Importable text packs for exams, coding, or workplace writing

---

## Tech Notes

- Built with plain HTML, CSS, and JavaScript.
- No required package manager.
- No required backend.
- Uses browser `localStorage` for persistence.
- Uses browser canvas for charts/visualisations.
- Uses optional service worker support for PWA-style caching.

---

## Repository Structure

Suggested structure:

```text
.
├── index.html
├── README.md
├── manifest.json        # optional, downloadable from app
├── sw.js                # optional, downloadable from app
└── screenshots/         # optional
```

---

## License

Add your preferred license here. If this is part of a public repo and you want open collaboration, the MIT License is a simple option.

---

## Credits

Created as an experimental, local-first typing coach focused on adaptive learning, privacy, and practical skill transfer.

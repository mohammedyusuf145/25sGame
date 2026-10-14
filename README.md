# تحدي 25 · Tahaddi 25

A two-team live classroom quiz show in **one self-contained file**: `tahaddi25.html`.
No internet, no installs, no external fonts, images or audio. Double-click the file to open it in Chrome, Edge, Safari or Firefox.

The game ships **without any questions**. You write them all in the built-in editor.

## How to use

1. **Open** `tahaddi25.html`.
   - **One screen** (laptop on the projector): just play. Press `H` to peek at the answer panel.
   - **Two screens**: click **Open display window** and drag the new window onto the projector, then click it once to enable sound and fullscreen. The first window becomes the **Host** panel with the answers. Sound plays on the display only.
2. **Add questions**: open **Question editor**. Pick a slot (Q1–Q18, 3 reserves, the Fast Decider) and write the question, four options and the correct letter. A badge on each slot shows *Empty*, *Incomplete* or *Ready*, plus a counter like "12/18 ready". Everything autosaves.
   - Use multiple **sets** (e.g. "Prep stage", "Ramadan"): new, rename, duplicate, delete.
   - **Export/Import JSON** to back up or share a set (same shape as `QUESTIONS_DATA` at the top of the file).
   - Print a **Judge sheet** (the answer key) or a blank **Score sheet**.
3. **New match**: name both teams, pick colours, add up to 10 students per team (or paste a list), and star a captain. Then flip the coin or choose who starts. With no students, the game plays team-level.
4. **Play a question**: the team picks a tile and you tap it. The timer **waits at 25** until you press **Start** (`Space`).
   - When the student announces a letter, tap that option (or press `A`–`D` / `1`–`4`) to lock it, then **Reveal** (`Enter`).
   - Wrong or out of time sends the question to a **steal**: the rival team gets 10 seconds, with the wrong option struck out, for half points.
5. **End**: when the board is cleared or the round limit is reached, the highest score wins. A tie goes to the Fast Decider. The winner screen can export results as JSON or print a results sheet.

## Host shortcuts

| Key | Action |
| --- | --- |
| `A`–`D` / `1`–`4` | Lock option |
| `Space` | Start / pause / resume the timer |
| `Enter` | Reveal or go to the next step |
| `Z` | Undo (multi-level) |
| `R` | Swap with a reserve question |
| `F` | Fullscreen |
| `M` | Mute |
| `H` | Answer panel (single-screen mode) |
| `?` | Help |

## Notes

- Your data lives in this browser's local storage: question sets, teams, the match in progress and settings. Use **Settings → Export all data** for a backup.
- Settings cover Arabic/English, Arabic-Indic or Western numerals, Dark Stage for bright rooms, reduce motion, volume sliders (master, music, effects), Reduce sound effects, negative points, option shuffle and number of rounds.
- **Custom sounds**: in Settings → Test sounds you can upload your own audio for any sound event. Reset returns it to the built-in synthesised sound.

## Hosting on Vercel

`vercel.json` serves the game at the site root (`/` → `tahaddi25.html`). In Vercel use **Framework Preset: Other**, leave **Build Command** and **Output Directory** empty, then redeploy.
- Projector: `https://<your-site>.vercel.app/#display`
- Host panel: `https://<your-site>.vercel.app/#host`

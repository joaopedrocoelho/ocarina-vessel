# Vessel · Ocarina Trainer

An installable web app for learning the 12-hole Alto C ocarina (built around the NIGHT by Noble layout, A=442).

- **Learn**: nine short lessons, from your first G to the subholes, the high notes, and sharps and flats
- **Fingerings**: every note from low A to high F, with sound, finger names, and editable fingerings
- **Tuner**: live pitch with a cents meter, plus a long-tone trainer (hold the note steady for 4 s)
- **Songs**: Step, Listen, and Follow modes. Follow listens to you and moves on when you hit each note.
- **Add a song**: paste letters (C D E, Do Re Mi, ドレミ), numbered 簡譜 (1=C 3 2 1…), or in-game ocarina buttons (A, C-down, C-right, C-left, C-up)

Works offline once it's installed. Songs, settings, and stats are saved in the browser on your phone.

## Put it online (the mic and install need HTTPS)

**GitHub Pages**
1. Create a repo, for example `vessel`, and push these files to `main` with this folder as the root.
2. In the repo, open Settings → Pages → Build and deployment, choose "Deploy from a branch", then pick `main` and `/ (root)`.
3. Open `https://<your-user>.github.io/vessel/` in Chrome on your Android phone.

**Netlify Drop**: drag this folder onto https://app.netlify.com/drop and open the URL it gives you.

## Install on Android
In Chrome, tap **Install app** at the top of Vessel, or use ⋮ → *Add to Home screen* → *Install*. Allow the microphone the first time you use the Tuner or Follow mode.

## Local testing
`npx serve .` (or `python3 -m http.server`), then open `http://localhost:<port>`. Browsers treat localhost as secure, so the mic works there.

## Updating
Edit the files and redeploy. If an installed copy keeps showing the old version, change `CACHE` in `sw.js` (for example to `vessel-v2`).

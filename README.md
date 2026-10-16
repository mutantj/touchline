# Touchline Coach Board

A soccer coaching web app: build lineups (5v5 to 11v11), manage your squad, move players on a tactics board, record plays, play them back and export animated GIFs.

It is a static site: plain HTML, CSS and JavaScript with no build step and no server code.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole app |
| `manifest.webmanifest` | Lets phones install it with "Add to Home Screen" |
| `sw.js` | Service worker that caches the app so it opens offline at the field |
| `icon-*.png`, `apple-touch-icon.png` | Home screen icons |

## Put it on GitHub Pages

1. Create a new repository on GitHub, for example `touchline`.
2. Upload all the files in this folder to the root of the repository (Add file, then Upload files).
3. Go to Settings, then Pages. Under "Build and deployment", choose "Deploy from a branch", pick `main` and `/ (root)`, then Save.
4. After a minute the app is live at `https://<your-username>.github.io/touchline/`.

Netlify and Cloudflare Pages also work: drag this folder onto their deploy page.

## Install on a phone

- **iPhone or iPad:** open the link in Safari, tap Share, then "Add to Home Screen".
- **Android:** open the link in Chrome, tap the menu, then "Install app" or "Add to Home screen".

## Where data is stored

Squads, lineups and saved plays are stored in the browser on each device (localStorage). Nothing is sent to a server. This means:

- Each phone or tablet has its own copy.
- Clearing the browser's website data deletes it.
- The app starts with an example squad. Use "Clear examples" in the Players tab to start your own.

## Updating

Edit `index.html`, then change `VERSION` at the top of `sw.js` (for example `touchline-v2`) so installed copies pick up the new version. Commit both files.

## Credits

Claude and MutantJ.

# Ezaz Risan — Portfolio

A single-page portfolio site for a graphic designer & WordPress front-end specialist. Built with plain HTML/CSS/JS — no build step, no dependencies.

## Structure

```
index.html          all markup, styles and scripts (single file, easy to edit)
assets/
  project-web-ads.jpg     Digital ad project image
  project-tote-bag.png    Tote bag project image
  project-wordpress.png   WordPress site project image
```

## Things to update before you publish

- **Email** — in `index.html` search for `hello@ezazrisan.com` and replace with your real email (it's used in two places: the button `mailto:` link and the visible text).
- **Social links** — in the Contact section, the Instagram and LinkedIn links are placeholders (`href="#"`). Swap in your real profile URLs. The Behance link points to `behance.net` — replace with your profile.
- **Behance project links** — "Year Planner Design" and "Poster Design" link directly to the Behance galleries you shared. Double check they still work.
- **Project images** — the `assets/` folder holds the three uploaded images. Swap them for higher-res exports if you have them, keeping the same filenames (or update the `src` in `index.html`).
- Add more projects any time by duplicating a `<article class="card">...</article>` block inside `#work`.

## Running locally

Just open `index.html` in a browser — no server required. Or, for live-reload while editing:

```bash
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Publishing on GitHub Pages

1. Push this repo to GitHub (see below).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Pick the `main` branch and `/ (root)` folder, then **Save**.
5. Your site will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

### Pushing from scratch

```bash
git init
git add .
git commit -m "Portfolio redesign"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

## Notes on the design

- Fonts: Fraunces (display) + Inter (body) + Space Mono (labels), loaded from Google Fonts.
- Fully responsive down to small phones; mobile gets a full-screen nav menu.
- Respects `prefers-reduced-motion` — the custom cursor, tilt effect and marquee are toned down/disabled for people who've set that preference.
- No frameworks, no build tools — just open and edit `index.html`.

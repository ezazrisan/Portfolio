# Ezaz Risan — Portfolio

A single-page portfolio site for a graphic designer & WordPress front-end specialist. Built with plain HTML/CSS/JS — no build step, no dependencies.

## Structure

```
index.html               all markup, styles and scripts (single file, easy to edit)
project-placeholder.jpg  shared photo currently used by all six work cards
```

No `assets` folder — every image lives at the top level of the repo, right next to `index.html`. This is deliberate: it removes the most common upload mistake (files landing outside a subfolder and breaking the image path).

## Adding your real project photos

All six cards in the Work section currently point to the same file, `project-placeholder.jpg`. To give a card its own photo:

1. Upload your new image straight to the repo root (same level as `index.html` — do **not** put it in a subfolder).
2. Open `index.html`, use Ctrl+F / Cmd+F to search for the card's title (e.g. `Year Planner`).
3. A few lines above the card's HTML, you'll find its CSS rule, e.g.:
   ```css
   .poster.p1{ background-image: url('project-placeholder.jpg'), linear-gradient(...); }
   ```
   Change `project-placeholder.jpg` to your new filename, keeping the quotes.
4. For the Web Ads, Tote Bag, and WordPress cards, there's also a "View full size" link lower down in that card's HTML block — update its `href` to match the same new filename so the link opens the right image.
5. Commit the change. Refresh your live site after a minute.

Each card's CSS rule is near the top of the file, easy to find by searching for `.poster.p1` through `.poster.p6` (in card order: Year Planner, Poster Design, Web Ads, Tote Bag, WordPress, Flyer Design).

## Things to update before you publish

- **Email** — search `index.html` for `hello@ezazrisan.com` and replace with your real email (used in the button `mailto:` link and the visible text).
- **Social links** — in the Contact section, the Instagram and LinkedIn links are placeholders (`href="#"`). Swap in your real profile URLs. The Behance link points to `behance.net` — replace with your profile.
- **Behance links on cards** — Year Planner and Poster Design already link to the galleries you shared. Flyer Design's link is still a placeholder `href="#"` — search for `Flyer Design` and replace the `#` with your real Behance link once it's up.
- Add more projects any time by duplicating a `<article class="card">...</article>` block inside `#work`.

## Fixing broken/missing images

If a card shows a broken icon or a plain color gradient where a photo should be:

1. **Check the file is in the repo root**, not inside a subfolder. Your repo's file list should show the image sitting next to `index.html`, at the same level.
2. **Check the filename matches exactly** what's written in `index.html` — GitHub Pages is case-sensitive, so `Photo.JPG` and `photo.jpg` are different files.
3. **Right-click the broken spot → Inspect** in your browser, find the `background-image` or `<img>` line, and click the path shown — it'll confirm whether it's a 404 and show the exact URL it tried.

## Running locally

Open `index.html` directly in a browser — no server required.

## Publishing on GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then **Save**.
4. Your site goes live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

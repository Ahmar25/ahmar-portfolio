# Portfolio site

A static, no-build portfolio site (plain HTML/CSS/JS) ready for GitHub Pages.

## File structure

```
.
├── index.html      # all page content and structure
├── css/
│   └── styles.css  # design tokens (colors, type) + layout
├── js/
│   └── main.js      # footer year only, no build step needed
└── README.md
```

## Deploy to GitHub Pages

1. Create a new GitHub repository (e.g. `ahmar-portfolio`).
2. Push these files to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, select **Deploy from a branch**.
5. Choose **Branch: main**, folder **/ (root)**, then **Save**.
6. GitHub will publish the site at:
   `https://<your-username>.github.io/<repo-name>/`
   (this can take a minute or two on first deploy).

If you want the site at `https://<your-username>.github.io/` directly (no
repo name in the URL), name the repository exactly
`<your-username>.github.io`.

## Updating content later

Everything is in plain HTML — no build step, no framework.

- **Projects**: edit the `<article class="card">` blocks inside the
  `#projects` section in `index.html`.
- **Tech stack**: edit the `<ul class="chip-list">` items inside the
  `#stack` section.
- **Contact links**: edit the `<ul class="contact-list">` items inside
  the `#contact` section.
- **Colors**: all defined once at the top of `css/styles.css` under
  `:root { ... }` — change a value there and it updates everywhere.

## Notes on content accuracy

Every project, skill, and detail on this site is drawn directly from your
CV and the two GitHub repositories you confirmed
(`flask-k8s-deployment`, `server-health-monitoring`). Three CV projects —
AWS Infrastructure Automation, Cloud Monitoring, and the Dockerized
Laravel Application — don't currently have a confirmed public repo, so
they're shown without a GitHub link. If you make those repos public
later, add a `<a class="card-link" href="...">View on GitHub ↗</a>` line
to that project's card, matching the pattern used on the other cards.

The `Ahmar25/Node.js` repository was intentionally left out because it
didn't clearly match a named CV project, and it currently has a file
(`Ahmar-key.pem`) committed that looks like a private key — worth
removing from that repo's history regardless of the portfolio.

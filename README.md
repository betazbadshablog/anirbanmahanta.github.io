# Anirban Mahanta — Portfolio

A fast, dependency-free portfolio site (plain HTML/CSS/JS) built for GitHub Pages.
Dark theme by default with a light-mode toggle, scroll animations, and an
animated "query console" hero.

## 1. File structure
```
├── index.html        → all page content & SEO tags
├── css/style.css      → theme tokens + layout + animations
├── js/script.js       → theme toggle, nav, scroll reveal, typing effect
├── assets/            → put your resume PDF, profile photo, og-image.png here
├── robots.txt
├── sitemap.xml
```

## 2. Deploy on GitHub Pages
1. Create a repo named exactly `anirbanmahanta.github.io` (this makes it your
   root user site — no `/repo-name/` in the URL).
2. Push these files to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/anirbanmahanta/anirbanmahanta.github.io.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages → Source → Deploy from branch → main / (root)**.
4. Your site goes live at `https://anirbanmahanta.github.io/` in a minute or two.

(If you'd rather use a normal repo name like `portfolio`, your URL will be
`https://anirbanmahanta.github.io/portfolio/` — in that case update the
`canonical`, `og:url`, and `sitemap.xml` URLs to match.)

## 3. Things to personalize before publishing
Search the files for `EDIT` / `<!-- EDIT -->` comments — these mark every spot
with placeholder content:

- **About** — your real story, goals, target roles.
- **Skills** — adjust the % values in `data-fill` to your honest level.
- **Projects** — replace the 4 sample cards with real projects + GitHub/live links.
- **Experience / Education** — real roles, dates, institutions.
- **Certifications** — real credentials + verification links.
- **Résumé button** — add `assets/resume.pdf`, then in `index.html` change:
  ```html
  <a href="#" class="btn btn-ghost" id="resumeBtn">
  ```
  to
  ```html
  <a href="assets/resume.pdf" class="btn btn-ghost" id="resumeBtn" download>
  ```
  and delete the `<span class="btn-note">` note next to it.
- **OG image** — add a real `assets/og-image.png` (1200×630) so links look good
  when shared on LinkedIn/WhatsApp.
- **Domain in meta tags** — `index.html`, `robots.txt`, and `sitemap.xml` all
  reference `https://anirbanmahanta.github.io/`. Update these if you use a
  custom domain.

## 4. SEO already set up
- Descriptive `<title>` / meta description / keywords
- Open Graph + Twitter Card tags for link previews
- `Person` JSON-LD structured data (helps Google understand who you are)
- Semantic HTML (`header`, `main`, `section`, `article`, `footer`)
- `robots.txt` + `sitemap.xml`
- Fully responsive, keyboard-accessible nav, respects `prefers-reduced-motion`

## 5. Local preview
Just open `index.html` in a browser — no build step or server required.
For live-reload while editing, you can optionally run:
```bash
npx serve .
```

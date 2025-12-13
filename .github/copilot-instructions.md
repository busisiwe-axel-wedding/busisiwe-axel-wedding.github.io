# Copilot instructions for this repository
Summary
- Static, multi-page wedding website built with plain HTML, CSS and image assets. No build system or server-side code. The repository is a GitHub Pages site: pushing `main` publishes to https://busisiwe-axel-wedding.github.io/.

Key files & layout
- Pages live in the repo root: `index.html`, `faqs.html`, `our-story.html`, `what-to-expect.html`, `our-recommendations.html`.
- Global styles: `style.css` (declares an `@font-face` for `fonts/CabinetGrotesk-Regular.otf`).
- Assets: `imgs/` (photos: .webp/.jpg/.jpeg), `fonts/`.

Big picture notes
- Purely static: header/logo/navigation markup is duplicated in each HTML file. Any global change to the header requires editing every page that contains it (see `index.html` and `our-recommendations.html`).
- Minimal JavaScript: `index.html` contains a small inline carousel that toggles elements with the class `.carousel-image` by setting `style.display = 'none'` / `style.display = 'block'`. Verify CSS selectors/classes before refactoring this script.

Repo-specific conventions
- Use relative links to files in the repo root (e.g. `<a href="our-recommendations.html">`). Renaming a page requires updating links in every HTML file that includes the header.
- Add images to `imgs/` and reference them with `imgs/<name>`. Prefer lowercase filenames without spaces to avoid cross-OS issues.
- Font assets are referenced from `fonts/CabinetGrotesk-Regular.otf` in `style.css`; preserve that path if you replace the font file.
- The copy contains a few minor typos (e.g. "Our Recomendations"). If you change visible text, scan for matching link text, alt attributes and filenames.

Concrete examples (from the codebase)
- Carousel: `index.html` has multiple `<img class="carousel-image" src="imgs/...">` and two buttons '#carousel-prev' and '#carousel-next' with inline JS that cycles visibility.
- Image-heavy page: `our-recommendations.html` shows how multiple `.webp` images are embedded and spaced — use it as the pattern for image sizing and margins.

Preview & developer workflow (local)
- No build step. To preview locally (PowerShell):

```powershell
# from repo root
python -m http.server 8000; Start-Process http://localhost:8000
```

- Alternatively use VS Code Live Server. Opening files via file:// may block local fonts in some browsers.

Deployment
- This is a GitHub Pages user/org site: deploy by pushing to `main`.
- There is no CI. If you add automation, document the build steps and where generated files should live (this site serves from the repo root today).

Quick checklist for edits
- Update the header nav in every `.html` file when adding/removing pages.
- Place images in `imgs/` and reference them with relative paths.
- Verify `style.css` edits don’t break the inline carousel (it depends on `.carousel-image` and display toggling).
- Keep filenames lowercase and avoid spaces.

Where to look first
- `index.html` — header structure + inline carousel JS
- `our-recommendations.html` — large image content pattern
- `style.css` — typography, layout and the `@font-face` declaration

If you want this file expanded with a PR template, commit guidelines, or a small preview script, tell me which area to expand and I will iterate.
# Copilot instructions for this repository

Summary
- This repository is a static, multi-page wedding website (plain HTML + CSS + image assets). No build system or server-side code is present. The repo is named `busisiwe-axel-wedding.github.io`, which is a GitHub Pages user/organization site — pushing `main` publishes the site at `https://busisiwe-axel-wedding.github.io/`.

# Copilot instructions for this repository

Summary
- This repository is a static, multi-page wedding website (plain HTML + CSS + image assets). No build system or server-side code is present. The repo is named `busisiwe-axel-wedding.github.io`, which is a GitHub Pages user/organization site — pushing `main` publishes the site at `https://busisiwe-axel-wedding.github.io/`.

# Copilot instructions for this repository

Summary
- Static, multi-page wedding site built with plain HTML, CSS and image assets. No build system, no server-side code. Repository is a GitHub Pages site: pushing `main` publishes to https://busisiwe-axel-wedding.github.io/.

Key files & layout
- Pages live in repo root: `index.html`, `faqs.html`, `our-story.html`, `what-to-expect.html`, `our-recommendations.html`.
- Global styles: `style.css` (also declares @font-face for `fonts/CabinetGrotesk-Regular.otf`).
- Assets: `imgs/` (photos: .webp/.jpg/.jpeg), `fonts/`.

Big picture notes
- Purely static: UI chrome (header/logo/nav) is duplicated across pages. Any global header change requires editing every HTML page that includes it (see `index.html` and `our-recommendations.html`).
- Minimal JS: there is an inline carousel in `index.html` that selects `.carousel-image` elements and toggles display via `style.display = 'none'|'block'`. Don't refactor that script without checking `style.css` and markup.

Repo-specific conventions
- Use relative links to files in the repo root (e.g. `<a href="our-recommendations.html">`). Renaming files requires updating all headers.
- Add images to `imgs/` and reference them as `imgs/<name>`. Prefer lowercase filenames without spaces.
- Font is loaded from `fonts/CabinetGrotesk-Regular.otf` in `style.css`; keep the path if replacing the font file.
- Copy has minor typos (e.g. header link text "Our Recomendations"). If correcting wording, update both link text and any matching filenames/alt text.

Concrete examples
- Carousel: `index.html` uses multiple `<img class="carousel-image" src="imgs/...">` and two buttons (`#carousel-prev`, `#carousel-next`) with inline JS that cycles visibility.
- Long content: `our-recommendations.html` demonstrates image-heavy content and uses many `imgs/*.webp` references—follow its markup for image sizing and spacing.

Preview & developer workflow
- No build step. To preview locally (PowerShell):

```powershell
# from repo root
python -m http.server 8000; Start-Process http://localhost:8000
```

- Alternatively use VS Code Live Server or open `index.html` in a browser (note: file:// may block local fonts in some browsers).

Deployment
- This is a GitHub Pages user/org site; deploy by pushing to `main`.
- There is no CI; if you add automation, document build steps and output location (site lives at repo root today).

# Copilot instructions for this repository

Summary
- Static, multi-page wedding website built with plain HTML, CSS and image assets. No build system or server-side code. Repository is a GitHub Pages site: pushing `main` publishes to https://busisiwe-axel-wedding.github.io/.

Key files & layout
- Pages live in repo root: `index.html`, `faqs.html`, `our-story.html`, `what-to-expect.html`, `our-recommendations.html`.
- Global styles: `style.css` (declares @font-face for `fonts/CabinetGrotesk-Regular.otf`).
- Assets: `imgs/` (photos: .webp/.jpg/.jpeg), `fonts/`.

Big picture notes
- Purely static: the header/logo/nav is duplicated across pages. To change global chrome, edit every HTML file that contains the header (see `index.html`, `our-recommendations.html`).
- Minimal JS: `index.html` includes a small inline carousel. It toggles `.carousel-image` elements with `style.display = 'none'|'block'`. Don't refactor that JS without checking `style.css` and the markup.

Repo-specific conventions
- Use relative links to files in the repo root (e.g. `<a href="our-recommendations.html">`). Renaming files requires updating all headers.
- Images live in `imgs/` and are referenced like `imgs/<name>`. Prefer lowercase filenames without spaces.
- Font is loaded from `fonts/CabinetGrotesk-Regular.otf` in `style.css`; keep that path when replacing the font file.
- Copy contains minor typos (example: header link text "Our Recomendations"). If fixing copy, update link text and matching attributes.

Concrete examples (copy from repo)
- Carousel: `index.html` uses multiple `<img class="carousel-image" src="imgs/...">` and two buttons (`#carousel-prev`, `#carousel-next`) with inline JS that cycles visibility.
- Image-heavy page: `our-recommendations.html` demonstrates many `imgs/*.webp` references; follow its markup for image sizing and spacing.

Preview & developer workflow (local)
- No build step. To preview locally (PowerShell):

```powershell
# from repo root
python -m http.server 8000; Start-Process http://localhost:8000
```

- Alternatively use VS Code Live Server or open `index.html` in a browser (note: file:// can block local fonts in some browsers).

Deployment
- This is a GitHub Pages user/org site — deploy by pushing to `main`.
- There is no CI; if you add automation, document build steps and output location (site currently lives at repo root).

Quick checklist for edits
- Update header nav in every `.html` file when adding/removing pages.
- Put images in `imgs/` and reference them with relative src paths.
- Verify `style.css` changes don’t break the inline carousel (it relies on `.carousel-image` and display toggling).
- Keep filenames lowercase and avoid spaces to reduce cross-OS issues.

Where to look first
- `index.html` — header structure + inline carousel JS
- `our-recommendations.html` — image-heavy content pattern
- `style.css` — typography, layout and the `@font-face` declaration

If you want this file expanded with PR templates, commit message guidance, or a short preview script, say which area to expand and I will iterate.
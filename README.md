# Rayad Naif Portfolio

A static, multi-page personal portfolio built with semantic HTML, reusable CSS variables, and lightweight vanilla JavaScript.

## Preview locally

Because this is a static site, you can open `index.html` directly in your browser, or run a tiny local server from the repository root:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Structure

- `index.html` — main portfolio hub (about, capabilities, selected projects, contact)
- `*.html` — individual case-study pages
- `assets/css/style.css` — shared visual system and responsive layouts
- `assets/js/main.js` — mobile nav toggle, reveal-on-scroll, and dynamic year
- `assets/img/favicon.svg` — site icon

## Content customization

- Update project copy and metadata directly in each case-study HTML file.
- Swap cover/gallery images by replacing each `img src` URL while keeping `width`, `height`, and meaningful `alt` text.
- For contact behavior, update the `mailto:` address in `index.html` and case-study pages.

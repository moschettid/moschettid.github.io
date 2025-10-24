# Personal Academic Website Template

Lightweight, responsive, accessible personal site scaffold for a CS student. Pure static (HTML/CSS/JS). No build step required.

## Structure

- `index.html` Main page with sections (hero, biography, research interests, activities, projects, skills, publications placeholder, contact).
- `css/style.css` Styling (dark theme, responsive, accessible focus, mobile nav).
- `js/main.js` Interactivity (mobile nav toggle, simple scroll reveal, dynamic activities timeline saved to `localStorage`, contact form demo, hide empty publications section).
- `assets/` Images & media (currently a profile SVG placeholder).

## Features

- Accessible semantic HTML & ARIA where relevant.
- Sticky header with responsive menu.
- Activities timeline with client-side add & persistence via `localStorage` (non-destructive, easy future backend hook).
- Publication section auto-hides until populated.
- Skill bars & tag pills for quick visual summary.
- Minimal JS (~4 KB min/gzip potential) and no dependencies.

## Getting Started

Open `index.html` directly in a browser, or serve locally for nicer dev:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Customization Checklist

1. Replace `Your Name` everywhere (title, header, hero, footer, alt text).
2. Update tagline & hero lead paragraph.
3. Swap `assets/profile-placeholder.svg` with a real photo (optimized ~200-400px square, compressed).
4. Edit biography paragraphs.
5. Adjust research interests (replace pill spans or generate dynamically later).
6. Populate projects (duplicate `.card` blocks or load from JSON).
7. Tune skill levels (data-level & span width percentages).
8. Remove or refine scroll reveal if prefers-static.
9. Configure real contact handling (static form backend like Formspree / Netlify Forms / serverless function).
10. When you have publications, add `<li>` items inside `#pub-list` then remove the automatic hide logic if you want it always visible.

### Publication Item Template

```html
<li class="pub-item">
  <span class="pub-authors">Your Name, Co Author</span> (2025).
  <strong>Title of the Work</strong>. <em>Conference/Journal</em>.
  <a href="paper.pdf">PDF</a>
</li>
```

## Adding Activities

Click "Add Activity"; entries store locally in the browser. To seed initial activities, you could hardcode an array in `main.js` or fetch from a static JSON file later.

## Future Enhancements

- Switch activities to JSON data file + fetch.
- Theming toggle (light/dark).
- Markdown-powered content via static site generator (optional).
- Add RSS/Atom feed for updates.
- Add structured data (JSON-LD) for person & scholarly article (when publications exist).
- Add simple build step for minification (esbuild) if desired.

## License

MIT — You may adapt freely. Attribution appreciated but not required.

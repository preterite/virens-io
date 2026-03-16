# virens.io

Technical documentation and download site for [VIRENS](https://virens.io) (Verdant Inquiry Research Environment for Scholars) — an open-source, modular research workflow framework for humanities scholars on macOS.

## What This Site Is

virens.io is the primary documentation and distribution hub for the VIRENS framework. It covers installation, configuration, module documentation, and community resources. It's the "how" of VIRENS — the practical counterpart to [verdantinquiry.org](https://verdantinquiry.org)'s philosophy.

## Local Development

```bash
cd ~/Sites/virens-sites/virens.io
bundle exec jekyll serve
# → http://localhost:4000
```

Requires Ruby and Bundler. Run `bundle install` on first setup.

## Content Structure

```
index.md              Landing page
about.md              About + colophon
contact.md            Contact information
_docs/                Documentation collection (output: true)
```

**Planned pages** (nav configured, content pending): Documentation, Downloads, Community

**Layouts:** `default.html` (pages), `doc.html` (docs collection)

**Docs collection:** Files in `_docs/` render to `/docs/:path/` with the `doc` layout.

## Shared Infrastructure

This site shares visual infrastructure with [verdantinquiry.org](https://github.com/preterite/verdant-inquiry) and [virens.me](https://github.com/preterite/virens-me):

- **Base CSS:** `assets/css/virens-base.css` (shared across all three sites, manually propagated)
- **Theme:** `assets/css/virens-dark-theme.css`
- **Fonts:** Cooper Hewitt (headings), Libre Baskerville (body), JetBrains Mono (code) — self-hosted woff2 in `assets/fonts/`
- **Includes:** Shared `header.html`, `footer.html`, `navigation.html`, `sidebar.html`, `breadcrumbs.html`

Cross-links to the other two sites appear in the navigation under "crosslinks."

For full infrastructure documentation, see the [VIRENS Websites Architecture Reference](https://github.com/preterite/virens-io) (maintained in the VIRENS development vault).

## Known Issues

- `github.repository` in `_config.yml` points to `preterite/SRE` — needs updating to `preterite/virens-io`
- Hosting not yet configured (GitHub Pages target)
- Index page references MIT License; framework repo uses AGPL-3.0 — license language needs reconciling
- `_mockup*.html` files are development artifacts, not content

## Related Sites

- [verdantinquiry.org](https://verdantinquiry.org) — Philosophy and methodology
- [virens.me](https://virens.me) — Development blog

## License

- **Code:** MIT License
- **Content:** CC BY-NC-SA 4.0

*Note: The VIRENS framework itself is licensed under AGPL-3.0. Website code and content licenses are separate.*

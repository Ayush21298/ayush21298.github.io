# ayushpatel.com

Personal website of **Ayush Patel** — Software Engineer at Samsung Electronics
(South Korea), IIT Delhi CSE graduate and President of the IIT Alumni
Association of Korea. Built with [Jekyll](https://jekyllrb.com/) and hosted on
GitHub Pages at [ayushpatel.com](https://ayushpatel.com).

## Stack

- Jekyll (`github-pages` gem — same versions GitHub Pages runs in production)
- No frameworks: hand-written CSS (`styles/site.css`) and vanilla JS
  (`scripts/site.js`), inline SVG icons
- Light/dark theme with system preference + manual toggle
- SEO: `jekyll-seo-tag`, `jekyll-sitemap`, `jekyll-feed`,
  `jekyll-redirect-from`, JSON-LD structured data, Open Graph / Twitter cards

## Develop locally

```bash
docker run --rm -it -v "$PWD":/site -w /site -p 4000:4000 ruby:3.1 \
  bash -c "bundle install && bundle exec jekyll serve --host 0.0.0.0"
# open http://localhost:4000
```

## Write a blog post

See [BLOGGING.md](BLOGGING.md) — add one Markdown file to `_posts/` and push.

## Layout map

| Path | Purpose |
| --- | --- |
| `index.html` | Homepage (hero, about, experience, projects, community…) |
| `blog/index.html` | Blog listing (`/posts.html` redirects here) |
| `_posts/` | Blog posts |
| `_layouts/`, `_includes/` | Templates, head/SEO, nav, footer, icons |
| `styles/site.css` | The whole design system |
| `scripts/site.js` | Theme toggle, mobile nav, scroll effects |
| `india-day-seoul-2026/` | Standalone event page |

# AGENTS.md

## Project Overview

This is **tmatsuzawa.github.io**, a Jekyll-based personal academic website showcasing research, publications, blog posts, and professional content. The site is deployed via GitHub Pages and serves as both a portfolio and research blog.

**Key Stack:** Jekyll (static site generator), Ruby Gems, HTML/CSS/JavaScript, Markdown

---

## Architecture & Content Structure

### Multi-Section Design
The site has distinct content sections, each with specific layouts and purposes:

- **Home/About** (`about.md`, `research.md`): Static pages using `layout: static_post`
- **Blog** (`_posts/`): Date-named markdown files (YYYY-MM-DD-title.md) using `layout: post`
- **Gallery** (`gallery.md`): Image showcase using `layout: gallery` with custom JS interaction
- **Special Pages** (`index.html`, `pubs.md`, `presentations.md`): Custom layouts for specific content

### Template Hierarchy
```
_layouts/default.html (base wrapper)
├── _includes/head.html (metadata, CSS imports)
├── _includes/header.html (navigation panel, mobile menu)
├── _includes/footer.html
└── [page-specific layout wraps this]
    ├── post.html (blog articles)
    ├── static_post.html (About, Research pages)
    ├── gallery.html (image gallery with custom CSS/JS)
    └── index_default.html (homepage)
```

### Content Metadata Pattern
All markdown files use **YAML Front Matter** with consistent structure:
```yaml
---
layout: [post|static_post|gallery|default]
title: Page/Post Title
category: [professional|personal|internal]
tags: ['tag1', 'tag2']
section-type: post  # optional, for blog posts
---
```

---

## Critical Developer Workflows

### Build & Serve Locally
```bash
# Install dependencies
bundle install

# Serve locally (http://localhost:4000)
bundle exec jekyll serve

# Build production site (outputs to _site/)
bundle exec jekyll build
```

### Deployment
Site auto-deploys to GitHub Pages via `gh-pages` branch. The `_config.yml` defines:
- URL: `http://tmatsuzawa.github.io`
- Build destination: `_site/`
- Pagination: 10 posts per page in `/blog/`
- Excluded files: README.md, Gemfile, Gemfile.lock

### Adding Content

**New Blog Post:**
1. Create file: `_posts/YYYY-MM-DD-slug-title.md`
2. Add YAML front matter with `layout: post`, `title`, `category`, `tags`
3. Write content in Markdown/HTML (both supported)
4. Images go in `images/blog/YYYY-MM-DD/` directory

**New Static Page:**
1. Create `.md` file in root directory
2. Use `layout: static_post`
3. Set `permalink: path/` to define URL structure
4. Header navigation in `_includes/header.html` links to these pages

---

## Project-Specific Conventions

### Naming & Organization
- **Blog images:** `images/blog/YYYY-MM-DD/image-name.jpg` (mirrors post date structure)
- **Special content images:** Organized by feature (e.g., `images/gallery/`, `images/chofse/`)
- **Favicons:** Standardized in `images/favicons/` with multiple sizes (144x, 192x, etc.)

### Content Type Categories
Posts use `category:` field with values like:
- `professional` – Research, publications, career content
- `internal` – How-to guides for site maintenance
- `personal` – Additional notes and resources

### Styling Pattern
- **Base theme:** `uno.css` (imported in `css/main.css`)
- **Code highlighting:** `monokai.css` (syntax highlighting for markdown code blocks)
- **Custom overrides:** Applied in `main.css` after imports (BEM-style class naming, e.g., `.btn-mobile-menu`, `.panel-cover--collapsed`)
- **Feature-specific CSS:** Gallery uses `css/gallery.css` (linked in layout, not globally)

### Mobile-First JavaScript
The `main.js` handles responsive navigation (jQuery-based):
- Mobile menu toggle: `.btn-mobile-menu` and `.navigation-wrapper`
- Navigation links trigger menu collapse on click
- Animations via CSS classes: `animated`, `bounceInDown`, `fadeIn`

---

## Integration Points & Dependencies

### Gems & Plugins
```ruby
source 'https://rubygems.org'
gem 'github-pages'        # Provides Jekyll + safe plugins for GitHub Pages
gem 'jekyll-spaceship'    # Extended Markdown parsing (tables, math, diagrams, etc.)
```

**Note:** Uses GitHub Pages' gem bundle, which restricts plugins to the GitHub Pages safe list. Custom plugins won't work in CI/CD.

### External Data Sources
- **Google Scholar ID:** `geBWMoIAAAAJ` (in `_config.yml` for future integration)
- **Social media:** GitHub, LinkedIn configured in `_config.yml`
- **Research DOIs:** bioRxiv and preprint links embedded directly in `research.md`

### Image Assets
All images are local (no CDN). Paths use Jekyll's `{{ site.url }}` and `| relative_url` filters to handle baseurl correctly. This is critical for GitHub Pages deployment where `baseurl:` might be empty.

---

## Key Files & Their Purposes

| File | Purpose |
|------|---------|
| `_config.yml` | Site metadata, build settings, pagination, author info |
| `_includes/header.html` | Navigation menu (spans, links, mobile toggle logic) |
| `_layouts/post.html` | Blog post wrapper (date, title, content) |
| `_posts/*.md` | Blog content (8 posts covering tutorials and research notes) |
| `about.md`, `research.md` | Static pages for biography and publications |
| `gallery.md` | Image gallery with inline HTML/CSS/JS |
| `css/main.css` | Custom styling for theme overrides |
| `js/main.js` | Mobile navigation interactivity (jQuery) |

---

## Common Patterns & Gotchas

### Front Matter Gotchas
- Blog posts MUST use `YYYY-MM-DD-` prefix in filename to be recognized by Jekyll's date logic
- `layout:` must match an actual file in `_layouts/` directory
- Empty `baseurl:` in `_config.yml` is intentional (top-level GitHub Pages site, not project site)

### Asset Path Handling
Always use filters:
- `{{ 'path/to/file' | relative_url }}` for links and assets
- `{{ site.url }}/path` for absolute URLs in embedded content
- Never hardcode `/images/...` paths (breaks if baseurl changes)

### Markdown Rendering
- Kramdown with GitHub Flavored Markdown (GFM)
- Hard wraps disabled (`hard_wrap: false`), so explicit `<br>` tags needed for line breaks
- Both Markdown and inline HTML work (see `research.md` and `gallery.md` examples)

### Navigation Links
Update `_includes/header.html` to add new top-level sections. Current sections:
- About (`/about/`)
- Research (`/research/`)
- Gallery (`/gallery/`)
- Publications (`/pubs/`)
- Blog (via pagination)

---

## Development Tips for AI Agents

1. **Before modifying content:** Check `_config.yml` for site settings and file exclusions
2. **When adding posts:** Ensure date format (YYYY-MM-DD) and proper YAML front matter or Jekyll won't process them
3. **For styling changes:** Look in `css/main.css` for custom overrides; theme base is `uno.css`
4. **For navigation:** Changes must be made in `_includes/header.html` (50+ lines of HTML with nested navs)
5. **For images:** Always place in logical subdirectories under `images/` and use `| relative_url` filter
6. **Testing locally:** Use `bundle exec jekyll serve` and check http://localhost:4000; watch terminal for build errors

---

## References

- **Jekyll Docs:** https://jekyllrb.com/docs/
- **GitHub Pages:** https://pages.github.com/
- **YAML Front Matter:** https://jekyllrb.com/docs/frontmatter/
- **Kramdown:** https://kramdown.gettalking.com/


# IequalsFt.github.io

Personal homepage + blog of Zhen Cui (Westlake University). Built as a plain Jekyll
site served by GitHub Pages — no theme gem, no build step locally.

## Structure

- `index.html` — homepage (hero, publications, CV, contact), front matter `home: true`
- `_layouts/` — `default.html` (all shared CSS + header/footer), `page.html`, `post.html`
- `_posts/` — blog posts. Filename: `YYYY-MM-DD-slug.md`. Front matter fields:
  - `title`, `date`, `tags`
  - `lang: en|zh` — each post has a paired translation
  - `alt_lang_url` — absolute path (`/blog/YYYY/MM/DD/slug/`) of the other-language version
- `blog/index.html` — post list
- `photo.jpg` — profile photo

## Writing a post

1. Create `_posts/YYYY-MM-DD-slug.md` (EN) and `_posts/YYYY-MM-DD-slug-zh.md` (中文), same date.
2. Set `lang` and cross-link via `alt_lang_url`. Permalink is `/blog/:year/:month/:day/:title/`
   (title from filename), so the EN post `2026-09-01-planar-dbr-workhorse.md` lives at
   `/blog/2026/09/01/planar-dbr-workhorse/` and its Chinese pair at
   `/blog/2026/09/01/planar-dbr-workhorse-zh/`.
3. Commit → push to `main` → Pages rebuilds automatically (~1 min).

## Local preview (optional)

```
gem install github-pages   # or: bundle
jekyll serve
```

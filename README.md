# IequalsFt.github.io

Personal homepage + blog of Zhen Cui (Westlake University). Built as a plain Jekyll
site served by GitHub Pages — no theme gem, no build step locally.

## Structure

- `index.html` — homepage (hero, publications, CV, contact), front matter `home: true`
- `_layouts/` — `default.html` (all shared CSS + header/footer), `page.html`, `post.html`
- `_posts/` — blog posts. Filename: `YYYY-MM-DD-slug.md`. Front matter fields:
  - `title`, `date`, `tags`
  - `lang: en|zh` — posts are written in either language, no pairing required
  - `alt_lang_url` — OPTIONAL: only if a post happens to have a translation, set it to
    the other version's absolute path (`/blog/YYYY/MM/DD/slug/`); omit otherwise
- `blog/index.html` — post list (Chinese posts get a `中文` tag automatically)
- `photo.jpg` — profile photo

## Writing a post

1. Create `_posts/YYYY-MM-DD-slug.md`, in whichever language you like (en or zh).
   Set `lang` accordingly. Only if you also write a translation, add `alt_lang_url`
   to both files cross-linking them.
2. Permalink is `/blog/:year/:month/:day/:title/` (title from filename), so
   `2026-09-01-planar-dbr-workhorse.md` lives at `/blog/2026/09/01/planar-dbr-workhorse/`.
3. Commit → push to `main` → Pages rebuilds automatically (~1 min).

## Local preview (optional)

```
gem install github-pages   # or: bundle
jekyll serve
```

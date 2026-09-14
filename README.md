# coffeemethod.github.io

My personal site, built with Jekyll and hosted on GitHub Pages.
Live at <https://coffeemethod.github.io>.

## Adding a blog post

1. Create `_posts/YYYY-MM-DD-your-title.md`.
2. Front matter at the top:

   ```yaml
   ---
   title: "Your title"
   date: 2026-09-14
   tags: [notes]
   description: "One sentence, used by search engines and the blog index."
   ---
   ```

3. Write markdown below it. Put `<!--more-->` after the opening paragraph to
   set where the excerpt cuts off.
4. Commit and push to `main`. The site rebuilds in about a minute.

`published: false` in the front matter keeps a draft out of the build.

## Adding a project

Edit `_data/projects.yml` and copy an existing block. Fields are `name`,
`description`, `url`, and `tags`. The Projects page builds itself from that file.

## Editing anything else

| What | Where |
| --- | --- |
| About page text | `index.md` |
| Site title, description, nav, links | `_config.yml` |
| Colors, fonts, layout | `assets/css/style.css` (the palette is at the top) |
| Page wrappers | `_layouts/` |

## Search engines

`jekyll-seo-tag` writes the title, description, canonical URL, Open Graph tags,
and JSON-LD into every page. `jekyll-sitemap` generates `/sitemap.xml`, which
`robots.txt` points at. `jekyll-feed` generates `/feed.xml` for RSS readers.
All three are built into GitHub Pages, so there's no build step to maintain.

After the first deploy, add the site to
[Google Search Console](https://search.google.com/search-console) and submit
`https://coffeemethod.github.io/sitemap.xml` once.

## Previewing locally (optional)

```sh
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>. Pushing works fine without ever doing this.

## Turning it on

Repo Settings → Pages → Build and deployment → Source: **Deploy from a branch**,
branch `main`, folder `/ (root)`.

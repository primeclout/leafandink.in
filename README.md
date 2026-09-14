# Leaf & Ink

One story a week.

## To publish a new issue

1. Add a file to `_posts/` named `YYYY-MM-DD-slug.md`.
2. Fill in the front matter, then paste the story below it. One blank line between paragraphs. No HTML needed.
3. Put any illustration in `assets/` and point `image:` at it.
4. Commit and push.

GitHub rebuilds the site. The new issue becomes the homepage and the previous one drops into `/archive/`. You never edit `index.html` or `archive.html`.

## Front matter

```yaml
---
title: "The Promise"
issue: "issue two"
kind: "Fiction"
minutes: 6
standfirst: "One line under the title. Write it last."
image: /assets/banyan.webp
image_alt: "Describe the picture for someone who cannot see it."
date: 2026-10-04
slug: the-promise
---
```

`image` and `image_alt` can both be left out; the figure disappears.

## Files

- `_config.yml` — site settings and the `/slug/` URL shape
- `_layouts/default.html` — the shell: head, fonts, all the CSS
- `_includes/issue.html` — one issue rendered; used by both the post page and the homepage
- `_layouts/issue.html` — wraps a post in the two above
- `index.html` — serves the newest post in full, no click, no redirect
- `archive.html` — lists every issue

## Before it goes live

The subscribe form posts to `#`. Change the `action` in `_includes/issue.html` to your Buttondown or Ghost endpoint.

## Running it locally (optional)

```
bundle install
bundle exec jekyll serve
```

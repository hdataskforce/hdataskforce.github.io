# hdataskforce.github.io

Website of the **IEEE Task Force on High Dimensional Data Analysis**, served by GitHub Pages at
<https://hdataskforce.github.io/>. Migrated from `hdataskforce.wordpress.com` in November 2026.

## Adding a news item

Create a file in `_posts/` named `YYYY-MM-DD-short-title.md` (you can do this in the GitHub web
editor: **Add file → Create new file**):

```markdown
---
title: "HDM'27: High Dimensional Data Mining Workshop"
tags: [workshop, call for papers]
---

We are organising ... Submission deadline: **1 August 2027**.
More at <https://example.org/hdm27>.
```

Commit it and the site rebuilds within a minute or two.

## Adding or editing a member

Each member is one file in `_members/` (the file name becomes the URL, e.g.
`_members/ata-kaban.md` → `/members/ata-kaban/`). Every field is optional except `name`:

```yaml
---
name: "Jane Doe"
role: "Vice-chair"          # optional, e.g. Chair; shown as a badge on the Members page
position: "Professor"
institute: "University of Somewhere"
institute_url: "https://..."
city: "Somewhere"
country: "UK"
email: "jane.doe [at] example ac uk"
website: "https://..."
---
```

Member photos are intentionally not published (PDPA).

## Other pages

`about.md`, `hdda-topics.md` and `materials.md` are plain Markdown. The navigation menu is
the `nav:` list in `_config.yml`. Layouts live in `_layouts/`, styles in `assets/css/main.css`.

## Previewing locally (optional)

```sh
gem install jekyll jekyll-sitemap
jekyll serve        # then open http://localhost:4000
```

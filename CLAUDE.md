# hdataskforce.github.io

Website of the **IEEE Task Force on High Dimensional Data Analysis**, live at
<https://hdataskforce.github.io/>. It's a Jekyll site built by GitHub Pages from `main` in the
`hdataskforce` GitHub org. It was migrated from hdataskforce.wordpress.com in November 2026.

## Rules (set by the Chair; keep them)

- **No member photos** anywhere on the site (PDPA).
- **No RSS/Atom feed.**
- **Leadership names appear only on the About page.** Keep them out of the footer and the home page.
- **Members are listed by first name.** `members.html` sorts on `name`, so don't add `order:` fields.
- **Name:** the task force is "High Dimensional Data **Analysis**". The HDM workshop series is
  deliberately "High Dimensional Data **Mining**". Don't "fix" either one.
- **Roles:** Jakramate Bootkrajang is Chair (since 2024) and Ata Kaban is Vice-chair (not co-chair).
- Keep the current academic theme. Don't reintroduce WordPress styling.
- **Old WordPress URL paths must keep working.** Posts use `/:year/:month/:day/:title/`, members use
  `/members/<slug>/`, and pages keep their old slugs (`/about/`, `/hdda-topics/`, `/materials/`, `/news/`).
- **GitHub Pages compatibility:** GitHub builds this with Jekyll 3.x and only its allow-listed plugins
  (currently `jekyll-sitemap`). Avoid Jekyll-4-only features and new plugins unless the site is
  switched to a GitHub Actions build.

## Layout

| Path | What |
|---|---|
| `_posts/YYYY-MM-DD-slug.md` | News items (front matter: `title`, optional `date`, `categories`, `tags`) |
| `_members/<slug>.md` | One file per member; front-matter fields only (see README.md) |
| `_data/leadership.yml` | Current and former leadership shown on the About page |
| `about.md`, `hdda-topics.md`, `materials.md` | Plain Markdown pages |
| `index.html`, `members.html`, `news.html`, `404.html` | Generated listing pages |
| `_layouts/`, `_includes/manifold.svg`, `assets/css/main.css` | Theme |
| `_config.yml` | Site settings and the `nav:` menu |

## Recurring chores

- **ICDM has a new website each year.** Update the ICDM link in `materials.md` when the next edition's
  site is announced.
- **New HDM workshop:** add a `_posts/` entry, and update the "What we do" HDM bullet in `about.md`
  to point to it.

## Workflow

- Preview: `jekyll serve --livereload` → http://localhost:4000 (needs `gem install jekyll jekyll-sitemap`).
- Publish: commit to `main` and push. Pages rebuilds in about a minute. Check the build with
  `gh api repos/hdataskforce/hdataskforce.github.io/pages/builds/latest --jq .status`.

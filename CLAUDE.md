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
- **GitHub Pages compatibility:** GitHub builds this with Jekyll 3.x and only its allow-listed plugins
  (currently `jekyll-sitemap`). Avoid Jekyll-4-only features and new plugins unless the site is
  switched to a GitHub Actions build.

## Layout

| Path | What |
|---|---|
| `_posts/YYYY-MM-DD-slug.md` | News items (front matter: `title`, optional `date`, `categories`, `tags`) |
| `_members/<slug>.md` | One file per member; front-matter fields only (see README.md) |
| `_data/leadership.yml` | Current and former leadership shown on the About page |
| `about.md`, `materials.md` | Plain Markdown pages (About includes the research topics) |
| `hdda-topics.html` | Redirect from the old `/hdda-topics/` URL to `/about/#research-topics` |
| `_data/activities.yml` | Every TF activity; feeds `/activities/` and the home page's "Recent activities" |
| `activities.md` | `/activities/`: lays out `_data/activities.yml` by type |
| `news.html` | `/news/`: archive of all posts; not in the menu (News was dropped as it duplicated Activities) |
| `hdm26.md` | `/hdm26/`: full HDM'26 workshop page (moved from the Chair's personal site) |
| `index.html`, `members.html`, `news.html`, `404.html` | Generated listing pages |
| `_layouts/`, `_includes/manifold.svg`, `assets/css/main.css` | Theme |
| `_config.yml` | Site settings and the `nav:` menu |

## Recurring chores

- **ICDM has a new website each year.** Update the ICDM link in `materials.md` when the next edition's
  site is announced.
- **New activity** (workshop, special session, tutorial, seminar): add an entry to `_data/activities.yml`
  (optionally with a `_posts/` entry or a full page to link to). For a new HDM workshop, also update the "What we do" HDM
  bullet in `about.md`; a full workshop page can live at `/hdmYY/` like `hdm26.md`.

## Workflow

- Preview: `jekyll serve --livereload` → http://localhost:4000 (needs `gem install jekyll jekyll-sitemap`).
- Publish: commit to `main` and push. Pages rebuilds in about a minute. Check the build with
  `gh api repos/hdataskforce/hdataskforce.github.io/pages/builds/latest --jq .status`.

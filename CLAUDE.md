# CLAUDE.md

Guidance for AI assistants working in this repository.

## What this repo is

A single-page Jekyll site hosted on GitHub Pages. The content is a Markdown
formatting exercise — a series of "Challenges" demonstrating italics/bold,
headers, links, images, blockquotes, lists, and paragraphs. There is no
application code, no build scripts, and no tests. GitHub Pages renders the
Markdown automatically.

## Layout

- `index.md` — the page rendered at the site root by Jekyll. Contains all
  the Markdown challenges.
- `README.md` — currently a byte-for-byte copy of `index.md` (it shows on
  the GitHub repo landing page).
- `_config.yml` — Jekyll config; sets `theme: jekyll-theme-cayman`. The
  cayman theme is the only supported customization here.

## Editing conventions

- `index.md` and `README.md` are intentionally kept in sync. When changing
  exercise content, update both files (or change one and copy it to the
  other). If you intentionally diverge them, call that out in the commit
  message so a future reader doesn't "fix" it back.
- Section headings use `## **Bolded Title**` and challenges are labeled
  with inline HTML: `<span style="color:blue">**Challenge I**</span>`.
  Preserve this style when adding new challenges.
- Challenges are numbered with Roman numerals (I, II, III, …) within each
  section.
- Link references (e.g. `[a fun place]: www.zombo.com`) deliberately lack
  the `https://` scheme — that's part of the exercise, not a bug. Don't
  "fix" them unless the task is specifically about making links work.
- The site is themed with `jekyll-theme-cayman`. Don't switch themes or
  add plugins without being asked — GitHub Pages restricts what's allowed.

## Workflows

- **Preview locally** (optional): `bundle exec jekyll serve` if Ruby/Jekyll
  is installed. There is no Gemfile checked in, so this is not the
  expected path — most contributors rely on the GitHub Pages render.
- **Publish**: push to `master`. GitHub Pages picks up the change
  automatically; there is no CI in this repo.
- **No tests, linters, or formatters** are configured. Don't add them
  unless the user asks.

## Git

- Default branch: `master`.
- This session's feature branch is `claude/claude-md-docs-dLtUO` per the
  task instructions. Commit and push work there, not directly to `master`.
- Only open a pull request when the user explicitly asks for one.

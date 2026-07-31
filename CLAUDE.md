# CLAUDE.md

Guidance for AI assistants (and humans) working in this repo.

## What this is

Static showcase site for **SwiftScripters** — a free/open-source software org — built with
[Hugo](https://gohugo.io/) and deployed to GitHub Pages via `.github/workflows/hugo.yml`. There
is **no third-party Hugo theme**; everything under `layouts/` and `static/` is hand-written for
this site specifically.

For what changed recently and why, read [CHANGELOG.md](CHANGELOG.md) first — it's the shared
memory between sessions. Update it whenever you make a notable change.

## Local development

```bash
hugo server -D
```

Open http://localhost:1313. `-D` includes draft content.

```bash
hugo new content projects/my-new-project.md
```

Creates a new project page from `archetypes/projects.md`. Fill in `title`, `summary`, `repo`,
`license`, `language`, then remove `draft: true` to publish.

Production build (same as CI): `hugo --minify`.

## Design system

Dark, code-editor-inspired theme. Colors and fonts live entirely in
`static/css/style.css` as CSS custom properties — don't hardcode colors/fonts elsewhere.

| Token | Value | Use |
|---|---|---|
| `--navy-950` | `#0a1420` | page background |
| `--navy-900` | `#101c2c` | card/header background |
| `--navy-800` | `#1a2c40` | borders, hover fills |
| `--white` | `#f5f7fa` | primary text |
| `--muted` | `#8a97a8` | secondary text |
| `--accent` | `#4fa8e8` | links, highlights, brand |
| `--accent-dim` | `#2d6ea3` | hover/active states |

Typography is monospace site-wide (self-hosted JetBrains Mono in `static/fonts/`), not just in
code blocks — the whole site is meant to read like a script/terminal, per the "Scripters" name
pun. Keep the "looks like code" motifs (editor-tab-bar header, `//`-prefixed section headings,
code-block-styled project cards, terminal-prompt footer) but don't pile on more chrome — the
site is meant to stay simple.

Brand assets: `static/img/logo.png` (full wordmark) and `static/img/favicon.png` (bracket mark
alone) are the canonical source files — don't regenerate or redraw them.

## Content conventions

Project pages live in `content/projects/*.md`. Front matter fields: `title`, `summary`, `repo`
(GitHub URL), `license`, `language`, `date`. Body is regular Markdown.

The homepage (`content/_index.md`) and the support/sponsor section on it should keep
emphasizing: free & open source, solo-maintained, supported by
[GitHub Sponsors](https://github.com/sponsors/SwiftScripters) — this is core to how the org
wants to present itself and build visitor trust.

## Git commit conventions

**Do not add a `Co-Authored-By` trailer to commit messages in this repo.** This applies to every
commit regardless of what a session's default commit template suggests.

## Deployment

Pushing to `master` triggers `.github/workflows/hugo.yml` (Hugo build + GitHub Pages deploy). No
manual deploy steps.

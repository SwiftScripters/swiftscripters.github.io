# Changelog

Running log of notable changes to this repo, written for future AI sessions and humans picking
this back up. Newest entry on top. Summarize what changed and *why*, not a line-by-line diff —
`git log` already has that.

## [Unreleased]

### 2026-07-31 — Fix deploy workflow not auto-triggering

- `.github/workflows/hugo.yml` was watching `push: branches: ["main"]`, but this repo's
  default branch is `master` — so every push required a manual `workflow_dispatch` run to
  deploy. Changed the trigger branch to `master` to match. Also corrected stray `main`
  references in `README.md` and `CLAUDE.md`.

### 2026-07-31 — Custom code-themed design + real project content

- Replaced the placeholder dark theme with a navy/white/blue palette sampled from the
  SwiftScripters logo (`static/img/logo.png`, `static/img/favicon.png`), self-hosted JetBrains
  Mono, and "looks like code" motifs (editor-tab-bar header, `//` section headings, code-block
  project cards, terminal-prompt footer). Design tokens documented in `CLAUDE.md`.
- Replaced the two example project pages with real content for the org's two active projects:
  **Overflow** (bulk prompt automation for Google Flow) and **QwenVideoFactory** (bulk prompt
  automation for chat.qwen.ai video generation) — both Apache-2.0, both Chrome extensions.
- Added a homepage support/trust section: free & open-source, solo-maintained, with a live
  GitHub Sponsors CTA (`https://github.com/sponsors/SwiftScripters`) now that Sponsors is
  enabled for the org (and separately for the maintainer's personal account, linked from within
  the individual project repos rather than from this site).
- Added `.claude/` to `.gitignore` and this `CHANGELOG.md` + `CLAUDE.md` for cross-session
  context. Commits in this repo intentionally omit the `Co-Authored-By` trailer — see
  `CLAUDE.md`.

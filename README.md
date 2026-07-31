# SwiftScripters Site

Static showcase site for SwiftScripters projects, built with [Hugo](https://gohugo.io/).

## Local development

```bash
hugo server -D
```

Then open http://localhost:1313

## Adding a new project

```bash
hugo new content projects/my-new-project.md
```

Edit the front matter (`title`, `summary`, `repo`) and the body, then remove `draft: true` when ready to publish.

## Deployment

Pushing to `master` triggers `.github/workflows/hugo.yml`, which builds the site with Hugo and deploys it to GitHub Pages automatically.

**One-time setup on GitHub:**
1. Push this repo to `SwiftScripters/swiftscripters.github.io` on GitHub.
2. In the repo, go to **Settings → Pages**.
3. Under "Build and deployment", set **Source** to **GitHub Actions**.
4. Push to `master` — the site will build and publish to `https://swiftscripters.github.io`.

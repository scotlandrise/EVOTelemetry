# EvoTelemetry website

One-page site built with [Hugo](https://gohugo.io), no theme needed.

## Run locally

```powershell
winget install Hugo.Hugo.Extended
hugo server
```

Open http://localhost:1313.

## Edit

| What | Where |
|---|---|
| Title, tagline, links, version | `hugo.toml` → `[params]` (replace `YOUR-USER`) |
| Intro text | `content/_index.md` |
| Feature cards | `data/features.yaml` |
| "How it works" steps | `data/steps.yaml` |
| Screenshot | `static/images/analyze.png` (16:9 works best) |
| Icon, favicon, link preview | `static/images/icon.svg`, `favicon.png`, `apple-touch-icon.png`, `social-card.png` |
| Colors and layout | `static/css/style.css` |

## Publish on GitHub Pages

1. Put this folder in a repository (or in a `site/` folder of the EvoTelemetry repo, then set `working-directory` in the workflow).
2. **Settings → Pages → Source: GitHub Actions**.
3. Push to `main`: `.github/workflows/hugo.yml` builds and publishes.

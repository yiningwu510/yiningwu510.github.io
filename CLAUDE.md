# Yining Wu Academic Website

## Architecture
- **Framework**: Hugo static site generator
- **Hosting**: GitHub Pages (auto-deploys on push to `main`)
- **Single source of truth**: `data/cv.yaml` drives all website content
- **CV**: `cv/cv.tex` is the LaTeX source; compiled PDF goes to `static/files/cv.pdf`

## How to Update Content

### Adding a new paper/publication
1. Add entry to `data/cv.yaml` under `publications:` or `working_papers:`
2. Add matching entry to `cv/cv.tex` in the appropriate section
3. Optionally add a figure image to `static/img/papers/` and reference it in the YAML `image:` field
4. If newsworthy, add to `news:` section in `data/cv.yaml`

### Adding a news item
1. Add entry to `data/cv.yaml` under `news:` (sorted by date, newest first)

### Updating teaching
1. Update `data/cv.yaml` under `teaching:` (instructor/lab_instructor/teaching_assistant)
2. Update `cv/cv.tex` teaching section

### Updating personal info
1. Update `data/cv.yaml` under `personal:`
2. Update `cv/cv.tex` header

### Updating CV PDF
1. Recompile `cv/cv.tex` to PDF
2. Copy new PDF: `cp cv/cv.pdf static/files/cv.pdf`

## Key Files
- `data/cv.yaml` - All structured content (single source of truth for website)
- `cv/cv.tex` - LaTeX CV source
- `static/files/cv.pdf` - Compiled CV PDF for download
- `static/img/YiningWu.jpg` - Profile photo
- `static/img/papers/` - Paper figure images (optional)
- `layouts/` - Hugo templates
- `static/css/style.css` - Stylesheet
- `hugo.toml` - Hugo configuration
- `.github/workflows/deploy.yml` - GitHub Pages deployment

## Local Development
```bash
hugo server -D    # Start dev server at http://localhost:1313
hugo              # Build to public/
```

## Update Workflow
When asked to update something (e.g., "add a new paper"):
1. Update `data/cv.yaml`
2. Update `cv/cv.tex`
3. If CV PDF needs updating, recompile and copy
4. Test with `hugo server`
5. Commit and push to deploy

# Yining Wu - Academic Website

Personal academic website built with [Hugo](https://gohugo.io/) and hosted on [GitHub Pages](https://pages.github.com/).

**Live site:** [https://yiningwu510.github.io](https://yiningwu510.github.io)

## Local Development

```bash
hugo server -D    # Start dev server at http://localhost:1313
hugo              # Build to public/
```

## Updating Content

All website content is driven by `data/cv.yaml`. Update that file to change what appears on the site.

The LaTeX CV source is in `cv/cv.tex`. After editing, recompile and copy:

```bash
cd cv && pdflatex cv.tex && cp cv.pdf ../static/files/cv.pdf
```

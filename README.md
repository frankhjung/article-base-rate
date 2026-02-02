# Article: Base Rate Explained

Live site: <https://frankhjung.github.io/article-base-rate/>

This repository contains the source and build tooling for the article "Base Rate
Explained."

## Source

Primary source file: [base-rate.Rmd](base-rate.Rmd)

## Build (Make)

Requirements:

- [pandoc](https://pandoc.org/)
- a TeX engine for PDF output (e.g.,
  [xelatex](https://www.overleaf.com/learn/latex/XeLaTeX)

Targets:

- `make` → builds HTML and PDF into `public/` directory
- `make clean` → removes the `public/` directory

## Output

- HTML: `public/index.html`
- PDF: `public/base-rate.pdf`

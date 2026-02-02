# Article: Base Rate Explained

Live site: <https://frankhjung.github.io/article-base-rate/>

An explanation of the base rate fallacy using COVID-19 hospitalisation data from
NSW Health (January 2022). This article demonstrates how misinterpreting
absolute numbers instead of rates can lead to incorrect conclusions about
vaccine effectiveness.

## Overview

This repository contains the source and build tooling for the article "Base
Rate: COVID-19 Hospitalisations."

### Key Topics

- Base rate fallacy in statistical interpretation
- Comparison of vaccination vs. non-vaccination hospitalisation rates
- Data visualisation with R and ggplot2

## Source

Primary source file: [base-rate.Rmd](base-rate.Rmd)

Additional files:

- [make.R](make.R) - R rendering script
- [files/article.css](files/article.css) - HTML styling
- [files/preamble.tex](files/preamble.tex) - LaTeX preamble for PDF

## Prerequisites

- [R](https://www.r-project.org/) (version 4.0 or higher recommended)
- R packages: `rmarkdown`, `ggplot2`, `knitr`
- [pandoc](https://pandoc.org/) (usually bundled with RStudio or rmarkdown)
- A TeX distribution for PDF output:
  - Linux: TeX Live (`sudo apt install texlive-xetex texlive-fonts-recommended`)
  - macOS: MacTeX
  - Windows: MiKTeX or TeX Live

### Installing R Packages

```r
install.packages(c("rmarkdown", "ggplot2", "knitr"))
```

## Building

### Using Make

```bash
# Builds both HTML and PDF
make

# Builds HTML only
make base-rate.html

# Builds PDF only
make base-rate.pdf

# Cleans generated files
make clean
```

### Using R Directly

```r
# From R console or RStudio
rmarkdown::render("base-rate.Rmd", "html_document")
rmarkdown::render("base-rate.Rmd", "pdf_document")
```

## Output Files

- **HTML**: `public/index.html` - web version with custom CSS
- **PDF**: `public/base-rate.pdf` - print version with LaTeX formatting

## Deployment

The article is automatically published to GitHub Pages via GitHub Actions when
changes are pushed to the `main` branch. See
[.github/workflows/pages.yml](.github/workflows/pages.yml) for the deployment
workflow.

## References

See the article itself for data sources and references to NSW Health reports and
related studies.

## [MIT License](LICENSE)

© Frank H Jung 2026

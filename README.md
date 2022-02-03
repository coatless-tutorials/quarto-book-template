# quarto-book-template
Template repository for creating a book powered by Quarto and Rendered by GitHub Actions onto GitHub Pages


## Overview

The repository holds: 

- [`.github/workflows/quarto-render.yml`](.github/workflows/quarto-render.yml): Install, setup, and render a Quarto book using R and Python
- [`_quarto.yml`](_quarto.yml): Setup the properties of the book in a minimal fashion (for more options see [Quarto: Book Structure](https://quarto.org/docs/books/book-structure.html))
- [`index.qmd`](index.qmd): Welcome page

Additional files:

- [`requirements.txt`](requirements.txt): List of Python Packages to install
- [`DESCRIPTION`](DESCRIPTION): List of R Packages using the standard DESCRIPTION file to install with `pak`.

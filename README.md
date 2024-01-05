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

## Publishing with GitHub Actions

Included in the repository is a custom GitHub Action that will automatically render and deploy the book onto GitHub Pages. 
Before the first run of the GitHub Action, please make sure to use locally in terminal the following:

```sh
quarto publish gh-pages
```

This command [initializes the `gh-pages` branch and turns on GitHub Pages for the repository](https://quarto.org/docs/publishing/github-pages.html#source-branch).

If you do not run this command before the first GitHub Action is triggered, you will likely encounter the following error message in the build log:

```sh
ERROR: No _publish.yml file available (_publish.yml specifying a destination required for non-interactive publish)
```

To avoid this issue, please make sure to run the GitHub Action locally so that GitHub can render and publish your Quarto document after every push to the repository.

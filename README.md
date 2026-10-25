# log

Personal notes on science, learning, and deep reinforcement learning.

This repository contains the source for the [Jupyter Book](https://jupyterbook.org/).

Once GitHub Pages is enabled for the `gh-pages` branch, the published book will
be available at <https://marabuuu.github.io/log/>.

## Build locally

If `uv` is not yet on your PATH in the current terminal, load its user-local
installation first. Then sync the locked dependencies and build the HTML book:

```bash
source "$HOME/.local/bin/env"
uv sync
uv run jupyter-book build docs
```

The built site will be available in `docs/_build/html/index.html`.

To open the local preview on macOS:

```bash
open docs/_build/html/index.html
```

The GitHub Actions workflow publishes the built HTML to the `gh-pages` branch.
In the repository settings, enable **Pages** with `gh-pages` as the branch and
`/ (root)` as the folder. After a push to `main` or `master`, the book will be
available at <https://marabuuu.github.io/log/>.

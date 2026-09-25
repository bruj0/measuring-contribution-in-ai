# When AI Writes the Code, What Counts as Contribution?

Source for the public essay hosted at
<https://bruj0.github.io/measuring-contribution-in-ai>.

- [`docs/index.md`](docs/index.md) is the canonical markdown source.
- The site is built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/)
  and the [`mkdocs-panzoom-plugin`](https://github.com/lichtwellicht/mkdocs-panzoom-plugin)
  via `.github/workflows/docs.yml`, which deploys to GitHub Pages on every
  push to `main`.

## Build locally

```bash
uv sync --extra docs
uv run mkdocs serve
```

Open <http://127.0.0.1:8000>.

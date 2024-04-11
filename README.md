# LEVANTE demographics data upload

## Install

Install [Quarto](https://quarto.org/docs/download/) (version 1.4.479 or higher).
Then install Python dependencies:
```
pip install -r requirements.txt
```

## Build

Use `quarto preview index.qmd` while developing app.

To make sure build works, run:
```
quarto render --output-dir _build
shinylive export _build _site
```

Then view the app locally with:
```
python3 -m http.server --directory _site --bind localhost 8008
```

App is automatically deployed using a [GitHub action](https://github.com/levante-framework/demographics/blob/main/.github/workflows/build-deploy.yml) to [GitHub pages](https://levante-framework.github.io/demographics/).

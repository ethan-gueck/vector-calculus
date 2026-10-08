# Multivariable & Vector Calculus

The Multivariable & Vector Calculus domain of [Ethan's NN](https://ethan-gueck.github.io/#nn): formulas built out as interactive pages, published at **https://ethan-gueck.github.io/vector-calculus/**.

**The Python in [`core/formula.py`](core/formula.py) is handwritten by Ethan Gueck.** The topic folders around it (solvers, pages and tests) are scaffolding that calls it.

Flashcard decks in this track: Multivariable & Vector Calculus. A neuron on the portfolio fills in once a topic here lists its card id in `cards`, and its **See how it works** button opens the topic's page.

## Site health

![Published site size against the 1 GB GitHub Pages limit](https://ethan-gueck.github.io/vector-calculus/health.svg)

The bar is the cumulative size of every file in the published site, where 100% is 1 GB, the most GitHub Pages will publish. [`.github/site_health.py`](.github/site_health.py) redraws it on every deploy.

## Topics

None yet: every neuron in this track shows its flashcard with **Coming soon**.

## Layout

```
vector-calculus/
├── <topic>/                  one folder per topic
├── core/formula.py           every neuron's mathematics, in flashcard order (empty sections until built)
├── tests/test_site.py        the site builds; topic cards are flashcard ids
├── pyproject.toml            [tool.portfolio-site]: site title and URL
├── .github/workflows/pages.yml   test, build and deploy on every push to main
└── .github/site_health.py      draws the published-site size bar shown above, on every deploy
```

Themes, styles, the page builder and the static API come from the shared [portfolio-projects](https://github.com/ethan-gueck/portfolio-projects) library (`general/`), installed from git.

```bash
uv sync                                   # install into .venv
uv run pytest                             # tests
uv run python -m general serve --port 8001   # build _site/ and preview it at http://localhost:8001
uv lock --upgrade-package portfolio-projects # pick up changes to general/
```

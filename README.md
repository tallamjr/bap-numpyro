![](https://github.com/tallamjr/bap-numpyro/workflows/CI/badge.svg)

# Bayesian Analysis in Python (2nd ed.) with Numpyro

<img src="https://static.packt-cdn.com/products/9781789341652/cover/9781789341652-original.png" width="150">

After discovering the fantastic
[`rethinking-numpyro`](https://fehiepsi.github.io/rethinking-numpyro/) project by
[@fehiepsi](https://github.com/fehiepsi), I was inspired to try and do something like that myself.
Primarily as a learning activity, this is my attempt at porting
[@aloctavodia](https://github.com/aloctavodia)'s "Bayesian Analysis in Python" [example PyMC3
code](https://github.com/aloctavodia/BAP) to [NumPyro](https://github.com/pyro-ppl/numpyro).

The port is now complete and modernised for 2026: all chapters (1-8) and exercises are ported, including newly-authored exercises for chapters 5-8 that do not exist in the original BAP repository.

## Setup

The project is managed with [uv](https://docs.astral.sh/uv/) and targets the following stack:

| Tool    | Version |
|---------|---------|
| Python  | 3.13    |
| NumPyro | 0.21    |
| JAX     | 0.10    |
| ArviZ   | 0.23    |

Create the environment:

```bash
uv sync --group dev
```

Run all notebooks as tests:

```bash
uv run pytest --nbmake notebooks/
```

Build the book locally:

```bash
uv run jupyter-book build .
```

### Running interactively in Jupyter Lab

The notebooks are configured to use a dedicated `bap-numpyro` kernel that points at the project's `.venv` interpreter. Register it once:

```bash
uv run python -m ipykernel install --user --name bap-numpyro --display-name "Python (bap-numpyro)"
```

Then launch Jupyter from the project environment and open any notebook:

```bash
uv run jupyter lab
```

Each notebook already selects the "Python (bap-numpyro)" kernel. Do not run them with a generic "Python 3" kernel: that may resolve to a different environment that lacks the pinned NumPyro/ArviZ stack and will raise import errors. If you see `ModuleNotFoundError: No module named 'numpyro'` (or `arviz`), the wrong kernel is selected: switch to "Python (bap-numpyro)" via Kernel > Change Kernel.

**Graphviz:** the model-rendering cell in the Chapter 2 exercises requires the `graphviz` system package. Install it with `brew install graphviz` (macOS) or `apt-get install graphviz` (Debian/Ubuntu).

**Float64:** the Gaussian Process chapter and its exercises call `numpyro.enable_x64()` for numerical stability. Ensure JAX float64 is not disabled in your environment.

## Acknowledgements

Many many thanks to [Du Phan](https://github.com/fehiepsi) for the foundations of which I have built
this from and [Osvaldo Martin](https://github.com/aloctavodia) for the amazing book: Bayesian Data
Analysis in Python

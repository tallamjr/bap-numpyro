[![Test Status](https://github.com/tallamjr/bap-numpyro/workflows/CI/badge.svg)](https://github.com/tallamjr/bap-numpyro/actions)

# Bayesian Analysis in Python (2nd ed.) with Numpyro

After discovering the fantastic
[`rethinking-numpyro`](https://fehiepsi.github.io/rethinking-numpyro/) project by @fehiepsi, I was
inspired to try and do something like that myself. Primarily as a learning activity, this is my
attempt at porting @aloctavodia's "Bayesian Analysis in Python" [example PyMC3 code](https://github.com/aloctavodia/BAP) to [NumPyro](https://github.com/pyro-ppl/numpyro)

I am still very new to `numpyro` myself, and therefore welcome comments and suggestions about how
best to write idiomatic code and translate things etc. My plan is to translate as much as possible
using _only_ `jax`, `arviz`, `numpyro` and `seaborn`.  There are aspects where I could not figure
out how to do it, maybe you can help?!

## How to read the notebooks

+ Read on the site: https://tallamjr.github.io/bap-numpyro/

+ Use GitHub's renderer: https://github.com/tallamjr/bap-numpyro/tree/master/notebooks/

+ Use Jupyter's nbviewer: https://nbviewer.jupyter.org/github/tallamjr/bap-numpyro/tree/master/notebooks/

## Acknowledgements

Many thanks to; [Du Phan](https://github.com/fehiepsi) for the foundations of which I have built
this from, [Osvaldo Martin](https://github.com/aloctavodia) for the amazing book: Bayesian Data
Analysis in Python, ...

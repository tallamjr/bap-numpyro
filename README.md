![](https://github.com/tallamjr/bap-numpyro/workflows/CI/badge.svg)

# Bayesian Analysis in Python (2nd ed.) with Numpyro

<img src="https://static.packt-cdn.com/products/9781789341652/cover/9781789341652-original.png" width="150">

After discovering the fantastic
[`rethinking-numpyro`](https://fehiepsi.github.io/rethinking-numpyro/) project by
[@fehiepsi](https://github.com/fehiepsi), I was inspired to try and do something like that myself.
Primarily as a learning activity, this is my attempt at porting
[@aloctavodia](https://github.com/aloctavodia)'s "Bayesian Analysis in Python" [example PyMC3
code](https://github.com/aloctavodia/BAP) to [NumPyro](https://github.com/pyro-ppl/numpyro)

🚧  **WIP** 🚧

_**NOTE**_ : This is still a work-in-progress project.

I am still very new to `numpyro` myself, and therefore welcome comments and suggestions about how
best to write idiomatic code and translate things etc. My plan is to translate as much as possible
using _only_ `jax`, `arviz`, `numpyro` and `seaborn`.  There are aspects where I could not figure
out how to do it, maybe you can help?!

#### TODOs:

- [] Fix Chapters 5, 6, 7
- [] Complete port of exercises 3 and 4
- [] Complete exercises for chapters 5, 6, 7 & 8
- [] Remove unused imports from each notebook

<!-- ## How to read the notebooks

+ Read on the site: https://tallamjr.github.io/bap-numpyro/

+ Use GitHub's renderer: https://github.com/tallamjr/bap-numpyro/tree/master/notebooks/

+ Use Jupyter's nbviewer: https://nbviewer.jupyter.org/github/tallamjr/bap-numpyro/tree/master/notebooks/ -->

## Acknowledgements

Many many thanks to [Du Phan](https://github.com/fehiepsi) for the foundations of which I have built
this from and [Osvaldo Martin](https://github.com/aloctavodia) for the amazing book: Bayesian Data
Analysis in Python

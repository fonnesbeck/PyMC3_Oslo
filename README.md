# Probabilistic programming in Python workshop 

**Oslo universitetssykehus HF, June 14, 2015**

Probabilistic Programming allows for automatic Bayesian inference on user-defined probabilistic models. Recent advances in Markov chain Monte Carlo (MCMC) sampling allow inference on increasingly complex models. This class of MCMC, known as Hamiltonian Monte Carlo, requires gradient information which is often not readily available. [PyMC3](https://github.com/pymc-devs/pymc3 "GitHub - pymc-devs/pymc3: Probabilistic Programming in Python. Uses Theano as a backend, supports NUTS and ADVI.") is a new open source Probabilistic Programming framework written in Python that uses [Theano](http://deeplearning.net/software/theano/ "Welcome &mdash; Theano 0.8.2 documentation") to compute gradients via automatic differentiation as well as compile probabilistic programs on-the-fly to C for better performance. Contrary to other Probabilistic Programming languages, PyMC3 allows model specification directly in Python code. This workshop will introduce new users to the PyMC3 package, and demonstrate how to implement and fit models.

## Schedule

| Time          | Activity                    |
| --------------|-----------------------------|
| 09:30-10:30 | **Introduction to PyMC3** |
| 10:30-10:45 | *Break* |
| 10:45-11:45 | **Model Building with PyMC3** |
| 11:45-13:00 | *Lunch* |
| 13:00-14:00 | **Model Checking and Output Processing** |
| 14:00-14:15 | *Break* |
| 14:15-15:15 | **Case Studies** |
| 15:15-15:30 | *Wrap-up* |

## Syllabus

### Introduction to PyMC3

* Variable types
* Step methods
* Variational inference methods

### Model Building with PyMC3

* Specifying priors and likelihoods
* Deterministic variables
* Custom variables
* Sampling and fitting

### Model Checking and Output Processing

* Storage backends
* Convergence diagnostics
* Goodness of fit
* Plotting and summarization

### Case Studies

* Hierarchical models of radon contamination
* Global burden of disease
* Survival modeling
* Machine learning: Clustering and neural networks

## Software Installation

Running PyMC3 requires a working Python interpreter, either version 2.7 (or more recent) or 3.4 (or more recent); we recommend that new users install version 3.5. A complete Python installation for Mac OSX, Linux and Windows can most easily be obtained by downloading and installing the free [`Anaconda Python Distribution`](https://www.continuum.io/downloads) by ContinuumIO. 

`PyMC3` can be installed using [`pip`](https://pip.pypa.io/en/latest/installing.html). The following command will install the most recent working version directly from the GitHub repository:

```bash
pip install git+https://github.com/pymc-devs/pymc3
```

PyMC3 depends on several third-party Python packages which will be automatically installed when installing via pip. The four required dependencies are: `Theano`, `NumPy`, `SciPy`, `Matplotlib`, and `joblib`. 

To take full advantage of PyMC3, the optional dependencies `seaborn`, `pandas` and `Patsy` should also be installed. These are *not* automatically installed, but can be installed by:

```bash
pip install seaborn patsy pandas
```

or, if you are running Anaconda, using the `conda` installer

```bash
conda install patsy pandas
```

Depending on which Anaconda installation you might have chosen, these may already have been installed.

### Windows Installation

If you are planning on using a Windows-based computer for the workshop, you may run into installation issues that are platform-specific. [Hans Olav has provided these instructions](http://datahans.blogspot.no/2016/04/installing-pymc3.html) for Windows users that may solve these issues.
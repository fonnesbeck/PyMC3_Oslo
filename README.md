# Workshop: Probabilistic Programming using PyMC3 

**Oslo universitetssykehus HF, June 14, 2016**

![Binder](http://mybinder.org/badge.svg)](http://mybinder.org/repo/fonnesbeck/PyMC3_Oslo)

Probabilistic Programming allows for automatic Bayesian inference on user-defined probabilistic models. Recent advances in Markov chain Monte Carlo (MCMC) sampling allow inference on increasingly complex models. This class of MCMC, known as Hamiltonian Monte Carlo, requires gradient information which is often not readily available. [PyMC3](https://github.com/pymc-devs/pymc3 "GitHub - pymc-devs/pymc3: Probabilistic Programming in Python. Uses Theano as a backend, supports NUTS and ADVI.") is a new open source Probabilistic Programming framework written in Python that uses [Theano](http://deeplearning.net/software/theano/ "Welcome &mdash; Theano 0.8.2 documentation") to compute gradients via automatic differentiation as well as compile probabilistic programs on-the-fly to C for better performance. Contrary to other Probabilistic Programming languages, PyMC3 allows model specification directly in Python code. This workshop will introduce new users to the PyMC3 package, and demonstrate how to implement and fit models.

## Schedule

| Time          | Activity                    |
| --------------|-----------------------------|
| 09:30-10:30 | **Introduction to PyMC3, MCMC** |
| 10:30-10:45 | *Break* |
| 10:45-11:45 | **Theano, Approximation Methods** |
| 11:45-13:00 | *Lunch* |
| 13:00-14:00 | **Model Building with PyMC3, Model Checking** |
| 14:00-14:15 | *Break* |
| 14:15-15:15 | **Case Studies** |
| 15:15-15:30 | *Wrap-up* |

## Syllabus

### Introduction to PyMC3

* Variable types
* Probability models
* Simple case studies

### Markov Chain Monte Carlo

* Metropolis sampling
* Gradient-based sampling methods

### Theano

* Tensors
* Automatic differentiation
* Operations

### Approximation Methods

* MAP
* Variational inference
* ADVI

### Model Building with PyMC3

* Specifying priors and likelihoods
* Deterministic variables
* Factor potentials
* Custom variables
* Step methods
* Generalized linear models
* Missing Data

### Model Checking and Output Processing

* Storage backends
* Convergence diagnostics
* Goodness of fit
* Plotting and summarization
* Seaborn

### Case Studies

* BEST
* Hierarchical models of radon contamination
* Global burden of disease
* Machine learning: Clustering and neural networks

## Software Installation

Running PyMC3 requires a working Python interpreter, either version 2.7 (or more recent) or 3.4 (or more recent); we recommend that new users install version 3.5 (but see special note below if you are a Windows user). A complete Python installation for Mac OSX, Linux and Windows can most easily be obtained by downloading and installing the free [`Anaconda Python Distribution`](https://www.continuum.io/downloads) by ContinuumIO. 

`PyMC3` can be installed using [`pip`](https://pip.pypa.io/en/latest/installing.html). PyMC3 also depends on several third-party Python packages which will be automatically installed when installing via pip. The four required dependencies are: `Theano`, `NumPy`, `SciPy`, `Matplotlib`, and `joblib`. To take full advantage of PyMC3, the optional dependencies `seaborn`, `pandas` and `Patsy` should also be installed. You can install PyMC3 and its dependencies by cloning this repository:

```
git clone https://github.com/fonnesbeck/PyMC3_Oslo.git
```

Then move into the directory created by the clone, and install the required packages using pip:

```bash
cd PyMC3_Oslo
pip install -r requirements.txt
```

Depending on which Anaconda installation you might have chosen, several or all of the required packages may already have been installed.

### Windows Installation

If you are planning on using a Windows-based computer for the workshop, you may run into installation issues that are platform-specific. [Hans Olav has provided these instructions](http://datahans.blogspot.no/2016/04/installing-pymc3.html) for Windows users that may solve these issues.
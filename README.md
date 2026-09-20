# Bayesian Flood Risk Modelling

**Bayesian Machine Learning**

`Python` · `PyTorch` · `Pyro` · `Bayesian Neural Networks` · `MCMC` · `Variational Inference` · `Laplace Approximation`

## Project Overview

Flood-risk prediction involves substantial uncertainty arising from complex
interactions between environmental, geographical and structural factors.

This project investigates the application of **Bayesian Neural Networks
(BNNs)** to flood-risk modelling, with a particular focus on comparing
different approaches to approximate Bayesian inference.

Three modelling approaches were explored:

- **Variational Inference** — approximating the posterior distribution
  through optimisation.
- **MCMC / NUTS** — sampling from the posterior distribution using
  Markov Chain Monte Carlo methods.
- **Laplace Approximation** — approximating the posterior around the
  maximum a posteriori solution.

The project explores not only predictive performance, but also the ability
of Bayesian methods to represent **uncertainty in model predictions**.

---

## Dataset

The project uses a flood-risk dataset containing environmental,
geographical and structural variables associated with flood susceptibility.

Features investigated during the modelling process include factors such as:

- Elevation
- Slope
- Impervious surface characteristics
- Vegetation / NDVI
- Distance to rivers
- Distance to roads
- Land-use characteristics
- Soil type
- Substrate
- Building characteristics

The dataset is included in the [`data/`](data/) directory to support
reproducibility of the modelling workflow.

---

## Methodology

### Data Preprocessing

The modelling workflow involved preparing the supplied flood-risk data for
Bayesian neural-network training, including feature selection, numerical
preprocessing and preparation of the target variable.

Class imbalance was also considered during the modelling process, with
techniques including **SMOTE** explored to improve representation of
under-represented classes.

### Bayesian Neural Networks

Unlike conventional neural networks, which learn a single set of model
weights, Bayesian Neural Networks treat model parameters probabilistically.

Instead of producing only a single deterministic prediction, the Bayesian
approach allows a distribution of possible model parameters and predictions
to be considered.

This makes it possible to investigate **predictive uncertainty** alongside
standard model performance.

---

## Approximate Bayesian Inference

### Variational Inference

Variational Inference approximates an otherwise difficult posterior
distribution using a simpler parameterised distribution.

The approximation is learned through optimisation, providing a scalable
alternative to directly sampling from the complete posterior.

### MCMC / NUTS

Markov Chain Monte Carlo provides a sampling-based approach to Bayesian
inference.

The project explores **No-U-Turn Sampling (NUTS)**, an adaptive extension
of Hamiltonian Monte Carlo that can efficiently explore complex posterior
distributions without manually specifying a fixed trajectory length.

### Laplace Approximation

Laplace Approximation provides another computationally practical approach
to uncertainty estimation by approximating the posterior distribution
around a fitted solution with a Gaussian distribution.

Together, these methods allow different trade-offs between computational
cost, posterior approximation and uncertainty estimation to be explored.

---

## Repository Structure

```text
bayesian-flood-risk/
│
├── data/
│   └── flood_data.csv
│
├── notebooks/
│   ├── 01_variational_inference.ipynb
│   ├── 02_mcmc_nuts.ipynb
│   └── 03_laplace_approximation.ipynb
│
├── report/
│   └── bayesian_flood_risk_report.pdf
│
├── .gitignore
└── README.md
```

---

## Technologies

**Programming:** Python

**Machine Learning:** PyTorch, Pyro, Scikit-learn

**Bayesian Methods:** Bayesian Neural Networks, Variational Inference,
MCMC, NUTS, Laplace Approximation

**Data Science:** Pandas, NumPy, feature engineering, class-imbalance
handling, uncertainty quantification

---

## Report

### Bayesian Neural Networks for Flood Risk Modelling

The accompanying coursework report provides a more detailed discussion of
the methodology, Bayesian inference techniques, experimental results and
interpretation of predictive uncertainty.

📄 **[Read the full project report](report/Report.pdf)**

---

## Author

**Nick Belemet**  
Mathematics & Data Science Graduate — University of Exeter

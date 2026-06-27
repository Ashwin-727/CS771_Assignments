# Machine Learning: SVMs, Generative Models, and EM

This repository contains three end-to-end algorithmic implementations developed for the CS771: Introduction to Machine Learning course at the Indian Institute of Technology (IIT) Kanpur (2025-26). The portfolio spans supervised linear margin classification, probabilistic generative modeling, and unsupervised mixture regression.

## Core Assignments and Methodologies

### 1. [SVM Hyperparameter Sensitivity Analysis](Assignment1)

An empirical investigation into the geometric properties and tuning dynamics of linear margin classifiers.

- **Geometric separability proof:** Demonstrated through geometric margin analysis that synthetically generated multi-cluster data is strictly linearly separable.
- **Systematic evaluation:** Analyzed LinearSVC stability across low, medium, and high difficulty regimes by shifting the regularization penalty (`C`), stopping tolerances (`tol`), and maximum iterations (`max_iter`).
- **Scaling behavior:** Empirically studied `O(nd)` training-time behavior and accuracy convergence across varying dataset sizes.

**Topics:** Linear SVMs, regularization dynamics, mathematical optimization, bias-variance tradeoff.

### 2. [Bayesian MNIST Image Reconstruction](Assignment2)

A probabilistic modeling framework developed to classify digits and reconstruct missing pixels using per-class Gaussian generative models.

- **Single-step joint MAP inference:** Formulated a Maximum A Posteriori (MAP) estimator that unifies classification objectives and pixel imputation in one joint optimization step.
- **Schur complement decomposition:** Applied Schur complement decomposition to the covariance matrix to derive a closed-form classification objective penalized by reconstruction uncertainty.
- **Optimized NumPy implementation:** Used vectorized computation and numerically stable routines such as `numpy.linalg.pinv` and `slogdet` to handle rank-deficient covariance matrices efficiently.

**Topics:** Gaussian generative models, MAP inference, Bayes' rule, Schur complements, numerical matrix stability.

### 3. [EM Mixture Regression for Air Quality Forecasting](Assignment3)

An unsupervised mixture modeling approach implemented to forecast ground-level ozone concentrations from environmental sensor data.

- **Mixture of Ridge regressors:** Derived and implemented the Expectation-Maximization (EM) algorithm to fit a finite mixture of Ridge regression models.
- **Complexity selection and ablation:** Evaluated convergence across model sizes and used feature ablation to identify dominant predictors.
- **Baseline comparison:** Compared mixture-regression performance with DecisionTreeRegressor baselines and analyzed component specialization across pollution regimes.

**Topics:** Expectation-Maximization, mixture models, Ridge regression, feature importance, decision trees.

## Academic Documentation

Each assignment directory contains a formal report named `report.pdf` and the corresponding submission archive:

| Assignment | Report | Archive |
| --- | --- | --- |
| Assignment 1 | [`Assignment1/report.pdf`](Assignment1/report.pdf) | [`Assignment1/minor1.zip`](Assignment1/minor1.zip) |
| Assignment 2 | [`Assignment2/report.pdf`](Assignment2/report.pdf) | [`Assignment2/minor2.zip`](Assignment2/minor2.zip) |
| Assignment 3 | [`Assignment3/report.pdf`](Assignment3/report.pdf) | [`Assignment3/minor3.zip`](Assignment3/minor3.zip) |

## Authors

**Group:** Team Optimizers 
**Course:** CS771: Introduction to Machine Learning  
**Institution:** Indian Institute of Technology (IIT) Kanpur, 2025-26

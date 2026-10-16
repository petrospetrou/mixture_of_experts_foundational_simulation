# Mixture of Experts — Interactive Mini Lab

An interactive, browser-based teaching lab exploring the foundations of **Mixture of Experts (MoE)** models. It walks through competitive learning in the original 1991 model, hierarchical mixtures and expectation-maximization (EM) in the 1994 extension, and the difference between learned gating and fixed-weight ensemble aggregation.

**[Open the interactive lab](https://petrospetrou.github.io/mixture_of_experts_foundational_simulation/)**

## Overview

The lab is designed to make the mechanisms behind MoE models visible and approachable. Rather than reproducing published experiments, it uses simplified, one-dimensional examples with interactive charts, sliders, step-by-step explanations, and optional mathematical details.

### What you'll explore

**1. Adaptive Mixtures of Local Experts (1991)**

- Why multiple simple experts can model patterns that one linear expert cannot.
- How a gating network assigns input-dependent probabilities to experts.
- How prediction error and gate probabilities combine into posterior **responsibilities**.
- How those responsibilities influence updates to the experts and gate.
- How specialization can emerge through repeated training.

**2. Hierarchical Mixtures of Experts (1994)**

- How nested gating networks form a hierarchy of expert paths.
- How path probabilities are calculated.
- How the **E-step** assigns posterior credit and the **M-step** refits the model.
- How repeated EM rounds change the model's predictions.

**3. Ensemble aggregation comparison**

- Fixed averaging versus input-dependent MoE weighting for regression.
- Majority voting versus gate-weighted class support for classification.
- Why this comparison illustrates *aggregation mechanisms*, rather than implementing full bootstrap-based bagging training.

## Run locally

No installation, build tools, package manager, or backend is required.

1. Download or clone this repository.
2. Open `index.html` in a modern web browser.
3. Use the navigation buttons, sliders, and training controls to explore the lessons.

The lab is self-contained, with its styles, scripts, and pre-rendered mathematical SVGs embedded in the HTML. It is designed to work offline.

## Scope and limitations

This project is an **educational simulation**, not an exact implementation or empirical reproduction of the cited papers. It uses illustrative targets and simplified models to explain gating, responsibilities, training, hierarchical routing, and aggregation. In the 1991 simulation, training uses a Gaussian-mixture likelihood objective, while the displayed mean squared error is a visual diagnostic. The comparison with bagging focuses on equal-weight averaging and voting; it does not perform bootstrap resampling.

## References

1. Jacobs, R. A., Jordan, M. I., Nowlan, S. J., & Hinton, G. E. (1991). *Adaptive Mixtures of Local Experts*. **Neural Computation, 3**(1), 79–87.
2. Jordan, M. I., & Jacobs, R. A. (1994). *Hierarchical Mixtures of Experts and the EM Algorithm*. **Neural Computation, 6**(2), 181–214.
3. Breiman, L. (1996). *Bagging Predictors*. **Machine Learning, 24**, 123–140.

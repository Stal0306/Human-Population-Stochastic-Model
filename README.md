# Stochastic Modeling of Human Population Growth

## Project Overview

This project explores long-term human population dynamics by extending the classical logistic growth model to include stochastic components. It models both continuous environmental variability and discrete catastrophic shocks using a stochastic differential equation (SDE) approach.

We use the Euler-Maruyama method to simulate population trajectories over 500 years, evaluating how random events such as pandemics and environmental fluctuations impact global population resilience and extinction risk.

---

## Objectives

- Model logistic population growth under uncertainty  
- Introduce environmental noise via a Wiener process  
- Simulate rare catastrophic events via a Poisson process  
- Perform sensitivity analysis on key parameters  
- Run Monte Carlo simulations to assess long-term stability  

---

## Model Description

The final SDE includes three main terms:

- Logistic growth term: `r * N * (1 - N / K)`
- Environmental variability (Wiener process): `β * N * dW_t`
- Catastrophic shocks (Poisson process): `J_t * N * dP_t`

Parameters are derived from World Bank data and historical shock frequencies. The model is solved numerically using the Euler-Maruyama method.

---

## Requirements

- Python 3.x  
- numpy  
- pandas  
- matplotlib  

Install dependencies:

```bash
pip install numpy pandas matplotlib
```

---

## How to Use

1. Ensure the CSVs are in the `data/` folder.  
2. Run `human_population_model.ipynb` to simulate and generate figures.  
3. Figures will be saved automatically in the `results/` folder.  

---


## Notes

- Sensitivity analysis shows key parameters like pandemic frequency, shock severity, and recovery rate have a critical impact on population stability.  
- Monte Carlo simulations reveal the range of possible outcomes and the importance of probabilistic modeling in demographic forecasting.

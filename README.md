# Time Series Modelling using Hidden Markov Models (HMM)
This project investigates the use of Hidden Markov Models (HMM) to identify latent regimes and structural changes in time series data, based on the GISTEMP temperature dataset (Northern Hemisphere surface temperature).

## Research Objective
The goal is to detect underlying latent states and assess whether regime-switching models can capture changes in temperature dynamics over time.

## Methodology
- Seasonal adjustment using STL decomposition  
- Estimation of Gaussian Hidden Markov Models with:
  - State-dependent means and variances  
  - State-dependent linear trends  
- Model selection using AIC, BIC, and log-likelihood  
- Regime decoding and analysis of state transitions  
- Subsample analysis (pre-1975 vs full dataset)  

## Key Findings
- Models with 4–6 states improve statistical fit, with a 5-state model offering the best balance between fit and interpretability  
- In the full sample, HMM states primarily capture the long-term upward trend rather than distinct regimes  
- In a more stationary subsample (pre-1975), regimes are more interpretable  
- Discrete-state models may struggle to represent smoothly evolving processes such as climate change  

## Limitations
- HMM assumptions (e.g. conditional independence) are not fully consistent with temperature dynamics  
- Rapid state switching suggests potential over-segmentation  
- Continuous trends are difficult to capture with discrete regimes  

## Tools
R (depmixS4, tidyverse, ggplot2)

## Project Structure
- `time-series-hmm.Rmd` – full analysis and modelling  
- `time-series-hmm-report.pdf` – concise report of results  

## Purpose
This project illustrates the strengths and limitations of regime-switching models in non-stationary time series, with applications to quantitative modelling and risk analysis.

# Option Pricing and Heston Calibration

This repository contains Python notebooks for pricing derivative products and calibrating a Heston stochastic volatility model to market option data.

## Contents

- `pricing.ipynb`  
  - Prices American put options (with dividends) using:
    - Binomial and trinomial trees
    - Black–Scholes PDE solved via a Crank–Nicolson scheme  
  - Computes Greeks (Delta, Gamma, Theta).  
  - Compares numerical methods with the Carr–Jarrow–Myneni (CJM) approach and studies convergence.

- `calibration.ipynb`  
  - Loads a panel of option prices (strike, maturity, market price).  
  - Implements the Heston model via Fourier/integration formulas.  
  - Calibrates Heston parameters by minimizing squared pricing errors.  
  - Uses the calibrated model to Monte Carlo–price a down-and-out barrier call and compares with Black–Scholes (including a control variate–style regression).

## Requirements

- Python 3.10+ (tested with 3.10 / 3.11)
- Recommended packages:
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `scipy`
  - `statsmodels`
  - `jupyter` (or JupyterLab)

Install via:

```bash
pip install numpy pandas matplotlib scipy statsmodels jupyter

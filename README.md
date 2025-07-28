 # VCV Risk Analysis
This repository contains Python modules for basic risk analysis including Value at Risk (VaR), Conditional Value at Risk (CVaR) and simple stress test u
tilities. The code is organized as a lightweight package under `src/` for easy r
e-use in notebooks or other scripts.
    
    Structure
    
   **src/data_loader.py** – Functions for downloading market data from yf
inance or loading from local CSV files.
     8  - **src/risk_metrics.py** – Helpers to compute VaR, CVaR and portfolio r
eturns.
     9  - **src/stress_tests.py** – Utilities for running historical stress test
s on a portfolio.
    10  - **ARCHITECTURE.md** – Outlines the overall package organization.
    11
    12  Example usage:
    13
    14  ```python
    15  from src import download_data, compute_var
    16
    17  prices = download_data(["AAPL"], start="2024-01-01", end="2024-06-30")
    18  var = compute_var(prices["Close"].pct_change().dropna())
    19  print("VaR:", var)
    20  ```
    21
    22  The repository currently contains several exploratory notebooks and samp
le CSV files used during development. These are not required for using the packa
ge but kept for reference.
    23

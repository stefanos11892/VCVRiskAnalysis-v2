# VCV Risk Analysis

This repository contains a small Python package for exploring basic risk metrics.
It provides helpers to download market data, calculate common statistics and run
simple stress tests.

## Repository layout

```
VCVRiskAnalysis-v2/
├── README.md
└── VCVRiskAnalysis/
    ├── ARCHITECTURE.md          # design notes
    ├── csv/                     # sample market data
    ├── src/                     # reusable package code
    │   ├── __init__.py
    │   ├── data_loader.py
    │   ├── risk_metrics.py
    │   └── stress_tests.py
    └── tests/                   # unit tests
```

The notebooks and CSV files under `VCVRiskAnalysis/` are left from
experimentation and are not required for using the package.

## Example

```python
from src import download_data, compute_var

prices = download_data(["AAPL"], start="2024-01-01", end="2024-06-30")
var = compute_var(prices["Close"].pct_change().dropna())
print("VaR:", var)
```

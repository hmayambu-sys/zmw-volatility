# Forecasting ZMW/USD Volatility
SSRN: 11727268 | Author: Henry Mayambu | Submitted to Bank of Zambia Working Papers
DOI transfer from SSRN 7029358 (ZAR/USD) to ZMW/USD

## Overview
Comparative study of GARCH(1,1), EGARCH(1,1), Stochastic Volatility (SV-MCMC), Random Forest, and LSTM for ZMW/USD daily volatility 2015-2026. Rolling out-of-sample 2020-2026.

Key result: Random Forest MSE 2.423 (-13.9% vs GARCH, DM -3.12***), SV-MCMC best QLIKE 0.182 for VaR / BoZ stress tests.

## Data
Source: Bank of Zambia daily rates + FRED DEXZAUS
Period: 2015-01-01 to 2026-06-30, T=2,987 obs
Returns: rt = 100 * ln(Pt/Pt-1)
File: data/zmw_usd.csv

## How to replicate
1. pip install -r requirements.txt
2. python src/forecast.py

## Results
See Table 2 in paper: Out-of-sample MSE/QLIKE and DM tests.
Regime split: Calm 2020-2021 vs Crisis 2022-2024 (Table 3).

## Disclaimer
Views are author's own, not BoZ. Replication code at https://github.com/hmayambu-sys/zmw-volatility

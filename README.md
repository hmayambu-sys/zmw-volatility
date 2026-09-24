# Forecasting ZMW/USD Volatility
SSRN: 11727388 | Author: Henry Mayambu | Submitted to Bank of Zambia Working Papers
DOI transfer from SSRN 1029558 (ZAR/USD) to ZMW/USD

## Overview
Comparative study of GARCH(1,1), EGARCH(1,1), Stochastic Volatility (SV-MCMC), Random Forest, and LSTM for ZMW/USD daily volatility 2015-2024. Rolling out-of-sample 2020-2024.

Key result: Random Forest MSE 2.423 (-13.9% vs GARCH, DM -3.12***), SV-MCMC best QLIKE 0.182 for VaR / BoZ stress tests.

## Data
Source: Yahoo Finance ZMW=X + Bank of Zambia daily rates (validated)
Period: 2015-01-02 to 2024-12-31
Observations: T=2604
Returns: rt = 100 * ln(Pt/Pt-1)
File: zmw_usd_daily_2015_2024.csv (also in /data/)

## Reproducibility
- requirements.txt lists all packages
- Data is in repo root and /data/
- Run: python -m src.forecast

## Link to BoZ
This repo supports BoZ Working Paper submission transferring methodology from ZAR/USD to ZMW/USD.

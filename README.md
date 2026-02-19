# TSMC-Derivatives-Analysis-Report
Consultancy style report for TSMC Options Chain Analysis with delta hedging based strategy backtesting.

This repository contains the code and analysis for a MSc Quantitative Finance group project at UCD Smurfit, focused on options on **Taiwan Semiconductor Manufacturing Company (TSMC)** listed on the NYSE. 

## Project overview

The notebook analyses TSMC’s options market using: 

- **Put–call parity** to identify theoretical arbitrage opportunities.   
- **Implied volatility estimation** via numerical inversion of the Black–Scholes–Merton model.   
- **Implied volatility surfaces** across strike and maturity.   
- **Delta‑hedging simulations** comparing implied‑volatility‑based vs historical‑volatility‑based hedging.   
- **Volatility trading** using at‑the‑money straddles based on the spread between implied and historical volatility. 

The work combines derivative theory (Hull, 2014) and literature on volatility skew with real options data and U.S. Treasury yields as the risk‑free rate. 

## Repository structure

- `TSMC-Derivatives-Analysis.ipynb`  
  Single Jupyter notebook containing the full workflow:   
  - Data loading and preprocessing for TSM equity and options, plus risk‑free rate.  
  - Put–call parity checks with a small tolerance (0.01 USD) to avoid arbitrage flags driven only by micro‑noise.   
  - Implied volatility estimation for calls and puts by solving Black Scholes Option Pricing Model.  
  - Construction and plotting of implied volatility vs strike curves and 3D volatility surfaces.   
  - Delta‑hedging simulations for a short call position using both implied and historical volatility.   
  - Volatility trade implementation via an ATM straddle based on the IV–HV spread. 

## My contribution

This project was completed as **Group 37 – FIN42020 Derivative Securities** (Etga Usta, Himanshu Ludhwani, Jasveen Kaur, Mi Hoang Vu, and Shubh Goela). 

**In this repository, the code and analysis are primarily my work (Shubh Goela):** 

- Designed and implemented the **Python notebook** used for all computations and visualisations.  
- Coded the full pipeline for:  
  - **Implied volatility** estimation from option mid‑quotes.   
  - **Volatility surface** construction and plotting for calls, puts, and combined surfaces.   
  - **Delta‑hedging simulations**, including daily hedge paths, share trading logic, cash‑flow tracking and P&L decomposition for implied‑volatility and historical‑volatility hedges.   
  - **Volatility trade (straddle)** logic based on the IV–HV spread and final payoff analysis.   
- Contributed to the written analysis and interpretation of the implied volatility and delta‑hedging sections of the report. 

The other group members contributed to data collection, put–call parity analysis, sections of the written report, and overall report assembly, as described in the project document. 

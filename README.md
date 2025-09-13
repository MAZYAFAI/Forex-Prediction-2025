# FX Forecasting with AutoML (AutoTS)

## 📌 Project Overview
This project investigates whether modern automated machine learning (AutoML) approaches can address long-standing challenges in foreign exchange (FX) forecasting, particularly the Meese–Rogoff puzzle. Using the **AutoTS framework**, we evaluate forecasting accuracy across **22 USD-based currency pairs**, comparing performance against the random walk benchmark.

## 🎯 Research Motivation
- Traditional models often fail to beat the random walk in out-of-sample forecasting (Meese–Rogoff puzzle).
- Deep learning models (e.g., LSTM, GRU) improve performance but require extensive data and expert tuning.
- AutoML offers a scalable, adaptive solution by automating preprocessing, model selection, and hyperparameter optimization.

## 🛠️ Methodology
1. **Data Collection & Preprocessing**
   - 22 USD-based currency pairs
   - Cleaned ND values, standardized datetime indices
   - Conducted stationarity testing (ADF) and applied differencing where necessary

2. **Modeling with AutoTS**
   - Automated pipeline for feature engineering, model selection, and tuning
   - Genetic algorithm search and ensemble modeling
   - Out-of-sample test set (~60 observations per pair) for evaluation

3. **Evaluation Metrics**
   - Mean Absolute Percentage Error (MAPE)
   - Symmetric Mean Absolute Percentage Error (SMAPE)
   - Root Mean Square Error (RMSE)

## 📊 Results
- **Average MAPE:** ~1.34% across all 22 currency pairs
- **18 out of 22 pairs** achieved sub-2% error rates
- Robust performance across developed, emerging, pegged, and commodity-linked currencies
- AutoTS consistently outperformed the random walk benchmark

## ✅ Key Contributions
- Comprehensive AutoML evaluation across multiple FX pairs
- Standardized preprocessing pipeline for FX time series
- Practical insights into real-world feasibility (hedging, portfolio overlay, VaR use cases)
- Identification of limitations and future research directions

## ⚠️ Limitations
- Analysis limited to **USD-based currency pairs**
- Models were static during the forecast horizon (no dynamic updates)
- Black-box ensemble models reduce interpretability
- No transaction cost or slippage analysis for trading applications

## 🚀 Future Work
- Extend evaluation to non-USD base pairs and cross-rates (e.g., EUR/GBP)
- Incorporate alternative data (macro, sentiment, commodities)
- Add explainability (e.g., SHAP, LIME) to improve transparency
- Walk-forward validation and dynamic model updating
- Backtesting with transaction costs and slippage

## 📂 Repository Structure
- `data/` → cleaned FX datasets
- `notebooks/` → exploratory analysis and preprocessing steps
- `scripts/` → AutoTS modeling and evaluation code
- `results/` → forecast outputs, evaluation metrics, and plots

## 📜 Citation
If you use this work, please cite:

*Author (2025). FX Forecasting with AutoML (AutoTS): Addressing the Meese–Rogoff Puzzle.*

# machine-learning-american-option-pricing-and-market-variable-prediction
# Machine Learning for American Option Pricing and Real-World Market Variable Prediction

## Overview

This project presents an end-to-end machine learning framework for American option pricing and financial market variable prediction. It combines quantitative finance, machine learning, and deep learning techniques to investigate two complementary problems:

- American option pricing using a hybrid structural-machine learning framework.
- Prediction of real-world market variables (Implied Volatility and Bid-Ask Spread) using live Apple (AAPL) option chain data.

The project was developed using Python and multiple machine learning frameworks as part of advanced financial machine learning research.

---

## Objectives

### Part 1 – American Option Pricing

Develop high-performance machine learning models capable of estimating American call option prices generated using a high-resolution Cox-Ross-Rubinstein (CRR) Binomial Tree.

### Part 2 – Real-World Market Variable Prediction

Build predictive models for:

- Implied Volatility (IV)
- Bid-Ask Spread

using real-world Apple Inc. (AAPL) option chain data.

---

# Repository Structure

```
├── American Option Pricing Paper.pdf
├── synthetic option pricing.ipynb
├── Real-World Option Chain Analysis.ipynb
├── american_call_option.csv
├── README.md
```

---

# Datasets

## Part 1

Synthetic American Call Option Dataset

- 31,173 option contracts
- Generated using a 15,000-step Cox-Ross-Rubinstein Binomial Tree
- Stratified sampling applied (10%)

Features include:

- Stock Price
- Strike Price
- Time to Expiry
- Risk-Free Rate
- Dividend Yield
- Volatility

---

## Part 2

Real-world Apple (AAPL) Option Chain

Collected using Yahoo Finance.

Final cleaned dataset:

- 2,380 option contracts

Features include:

- Strike Price
- Days to Expiry
- Moneyness
- Open Interest
- Volume
- Bid
- Ask
- Implied Volatility
- Spread Percentage

---

# Machine Learning Models

## Classical Machine Learning

- Linear Regression
- Ridge Regression
- Random Forest
- Gradient Boosting Machine
- Support Vector Regression (SVR)
- XGBoost

## Deep Learning

- TensorFlow/Keras Neural Network
- PyTorch Neural Network
- Multi-Layer Perceptron (MLP)

---

# Hybrid Structural-ML Framework

Instead of directly predicting American option prices, the project introduces a hybrid approach:

American Option Price

=

Black-Scholes European Price

+

Predicted Early Exercise Premium (EEP)

This significantly reduces prediction complexity while improving model accuracy.

---

# Feature Engineering

Examples include:

- Log Moneyness
- sqrt(T)
- Volatility × sqrt(T)
- Interest Rate × Time
- Dividend Yield × Time
- Moneyness × Volatility
- Moneyness × Time

For real-world option chains:

- Days to Expiry
- Bid-Ask Spread
- Mid Price
- Spread Percentage
- Moneyness
- Option Type

---

# Hyperparameter Optimisation

- Grid Search Cross Validation
- Bayesian Optimisation

---

# Evaluation Metrics

Models were evaluated using:

- R² Score
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Percentage Error (MAPE)

---

# Key Results

## Part 1

Hybrid XGBoost + Black-Scholes achieved

- R² ≈ 0.9999
- MAE < $0.05

showing that learning only the Early Exercise Premium substantially improves pricing accuracy compared to direct prediction.

---

## Part 2

### Implied Volatility Prediction

Best Model

Random Forest

R² = 0.5352

---

### Bid-Ask Spread Prediction

Best Model

Neural Network

R² = 0.8988

---

# Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- TensorFlow
- PyTorch
- SciPy
- Matplotlib
- Seaborn
- yfinance

---

# Applications

- Quantitative Finance
- Option Pricing
- Financial Machine Learning
- Market Microstructure Analysis
- Algorithmic Trading Research
- Derivatives Analytics

---

# Future Improvements

- Multi-asset option pricing
- Heston stochastic volatility model
- Jump diffusion models
- Differential Machine Learning
- Greeks prediction
- Reinforcement learning for derivatives pricing

---

# Author

**Aswin Thanjavur Sivaprakasam**

MSc Financial Technology  
National College of Ireland

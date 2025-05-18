# 📉 SEO Underpricing Classification – A FinTech Approach

This project aims to classify **Secondary Equity Offerings (SEOs)** based on the likelihood of underpricing. The goal is to support investment decision-making and proprietary trading strategies by identifying patterns and predictors associated with SEO underpricing in U.S. capital markets.

---

## 📌 Project Overview

**Business Objective:**  
To build a predictive model that flags SEOs likely to be underpriced using machine learning techniques and financial market indicators. This can help investment branches:

- Anticipate undervalued opportunities
- Hedge against macroeconomic uncertainty
- Optimize liquidity and risk management

---

## 📂 Datasets Used

| Dataset | Description |
|--------|-------------|
| **SEO CRSP Dataset** | Security-level data on SEOs from the Center for Research in Security Prices (CRSP) |
| **S&P 500 Index Return** | Daily return values for the S&P 500 |
| **S&P 500 Volatility Index (VIX)** | Market volatility indicator |
| **Consumer Price Index (CPI)** | U.S. inflation measure |
| **US 1-Month Treasury Rate** | Proxy for short-term interest rates |

All external datasets were sourced from [Wharton Research Data Services (WRDS)](https://wrds-www.wharton.upenn.edu/) and [FRED](https://fred.stlouisfed.org/).

---

## 🔍 Exploratory Data Analysis (EDA)

- Removed IPOs and non-U.S. listings
- Handled missing values and duplicates
- Created lag-based features (e.g., lagged stock price, lagged market indicators)
- Engineered features like **deal size as % of market cap**

---

## 🧪 Feature Selection

- Used **Random Forest** to identify the top 20 predictive features
- Also evaluated feature importance using **LightGBM**
- Key features included:  
  - One-month lagged deal size  
  - Lagged S&P 500 return  
  - Lagged VIX  
  - Market capitalization  
  - Interest rates  

---

## ⚙️ Model Development

We trained and compared multiple classification models:

- **Logistic Regression**
- **Random Forest Classifier**
- **LightGBM (Gradient Boosting)**
- **XGBoost**

Final model selection was based on performance metrics such as accuracy, F1-score, precision, and recall.

---

## 📈 Results & Business Insights

**Key Findings:**
- Market volatility (VIX) and lagged macroeconomic indicators significantly influence underpricing likelihood
- Smaller deals (relative to market cap) tend to be more underpriced
- Lagged equity market performance has a predictive relationship

**Strategic Recommendations:**
- **Use derivatives** like call options to hedge against market volatility
- **Adopt long-short strategies** based on underpricing predictions
- **Avoid overexposure** to a single SEO event
- **Implement staggered stop-loss and take-profit levels**

---

## 🚧 Limitations & Future Work

| Current Limitations | Future Improvements |
|---------------------|---------------------|
| Small sample size   | Expand to global SEO markets |
| Limited macro data  | Incorporate sentiment & news data |
| Company-level features lacking | Add balance sheet & industry indicators |

---

## 📎 References

- CRSP/Compustat Merged Database – WRDS  
- FRED – U.S. Economic Indicators  
- OpenAI ChatGPT (2024) – Support for exploratory insights

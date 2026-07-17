# Customer Conversion Prediction for Bank Marketing — ML Classification

**ROC AUC = 0.815 · Finds ~65% of actual subscribers · Explainable predictions (SHAP)**

## 🎯 The Challenge

A bank runs phone campaigns selling term deposits, but only ~11% of calls end in success — the call center wastes resources on clients who won't subscribe.

## ⚙️ The Solution

Using data on 41K clients (profile, contact history, economic context), I:

- Ran full exploratory analysis and feature engineering
- Tested 5 ML algorithms (Logistic Regression, kNN, Decision Tree, LightGBM with hyperparameter tuning)
- Added business rules — e.g., stop calling after 5 attempts, since more calls almost never convert
- Made every prediction explainable with SHAP — the bank sees *why* each client got their score

## 📈 The Result

- The model ranks clients by likelihood to subscribe — the bank calls the most promising first
- Fewer wasted calls, higher campaign conversion
- Every decision can be explained to business stakeholders in plain terms

## 🔢 Metrics

| Metric | Value |
|---|---|
| ROC AUC | 0.815 (best of 5 algorithms) |
| Recall (subscribers found) | ~65% |
| F1 after business rules | 0.50 → 0.53 |

## 🛠 Tech Stack

Python · scikit-learn · LightGBM · Hyperopt · SHAP · Pandas · Seaborn

---

🔗 **Full technical implementation:** [bank-marketing-prediction](https://github.com/darinaze/Bank-marketing-prediction-)

*Built on the open UCI Bank Marketing dataset.*

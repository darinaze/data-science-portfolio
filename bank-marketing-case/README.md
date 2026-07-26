# 🏦 Customer Conversion Prediction for Bank Marketing

> **In one line:** A machine learning model that tells a bank *which clients are worth calling* — so the sales team stops wasting time on people who will never say yes.

![Customer Conversion Prediction cover](../cover2_Conversion_Prediction_v2.png)

**ROC AUC = 0.815 · Finds ~65% of real subscribers · Every prediction explained (SHAP)**

---

## 🎯 The problem (in plain words)

A bank sells term deposits by calling people. But it works only about **11% of the time** — so roughly **9 out of 10 calls are wasted** on clients who were never going to subscribe. That is a lot of the sales team's time, salary, and patience spent for nothing.

**The question the bank needed answered:** *Who should we call first?*

![Before — calling everyone wastes time and money](../case_problem_before.png)

---

## 💡 What I built

I built a model that looks at each client and gives a simple score: **how likely are they to subscribe?** The team can then start with the most promising people and skip the ones who almost certainly won't convert.

Two things make it useful in real life, not just on paper:

- **It explains itself.** For every client, the model shows *why* it gave that score (age, previous contact, economic context, etc.). The bank isn't asked to trust a black box — it sees the reasons. *(This uses SHAP.)*
- **It respects common sense.** I added business rules on top of the model — for example, stop calling a client after 5 attempts, because more calls almost never convert and just annoy people.

<details>
<summary>🔧 Under the hood (for technical readers)</summary>

- Data on **41K clients** (profile, contact history, economic indicators) — open UCI Bank Marketing dataset.
- Full exploratory data analysis (EDA) and feature engineering.
- Compared **4 algorithms**: Logistic Regression, k-Nearest Neighbours, Decision Tree, and **LightGBM** with hyperparameter tuning (Hyperopt) — LightGBM won.
- Model explainability with **SHAP**; business rules applied on top of the raw scores.

</details>

---

## 📈 The impact

![After — the model picks who to call, most say yes](../case_solution_after.png)

| What the bank gets | Result |
|---|---|
| Catches most future subscribers | **~65% of real subscribers found** (recall) |
| Ranks clients so the best are called first | **ROC AUC = 0.815** (best of 4 models) |
| Fewer wasted calls after business rules | **F1 improved 0.50 → 0.53** |
| Trust & transparency | Every prediction **explained with SHAP** |

**Bottom line:** instead of dialing everyone and converting ~11%, the team calls a shorter, smarter list and still reaches about two-thirds of the people who would actually subscribe — less time wasted, higher conversion per call.

---

## 🖼 Visuals

<!-- Заміни назви файлів на свої реальні картинки з папки кейсу -->

**What drives a client's decision (SHAP):**
<!-- ![SHAP feature importance](./shap_summary.png) -->

**Why LightGBM won (model comparison):**
<!-- ![Model comparison](./model_comparison.png) -->

> Розкоментуй рядки вище і встав назви своїх файлів-графіків (вони вже є в цьому кейсі).

---

## 🛠 Tech stack

Python · pandas · scikit-learn · **LightGBM** · Hyperopt · **SHAP** · Seaborn

## 📂 In this repo

- `…` — notebook/code (EDA, modelling, evaluation)
- `…` — SHAP and model-comparison charts
- Data: open **UCI Bank Marketing** dataset

🔗 **Full technical implementation:** [bank-marketing-prediction](https://github.com/darinaze) · ⬅️ [Back to portfolio](../README.md)

---

*Built by Daryna Zelenska — Data Scientist · Machine Learning Engineer. Need a model that predicts customer behaviour and explains itself? Let's talk.*

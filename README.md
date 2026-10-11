<div align="center">

# 📈 Rossmann Store Sales Forecasting

*An end-to-end Machine Learning pipeline for retail sales prediction using XGBoost and Optuna.*

</div>

## 📌 Overview

This repository contains a complete machine learning solution for forecasting daily sales across **1,115 Rossmann drugstores**. The approach leverages a global **XGBoost Regressor** enhanced by rigorous feature engineering and automated hyperparameter tuning via **Optuna**, achieving an **RMSPE of 0.10385** on the Kaggle leaderboard.

---

## 🛠️ Key Pipeline Steps

* **Data Preprocessing**: Handled missing values, filtered out closed-store days, and formatted temporal data.
* **Feature Engineering**: Extracted cyclical temporal indicators, promotional duration metrics, and lag/rolling sales statistics across store groups.
* **Hyperparameter Optimization**: Deployed Optuna (Bayesian Optimization) to fine-tune key tree-building parameters (`max_depth`, `learning_rate`, `subsample`, `colsample_bytree`).
* **Modeling & Evaluation**: Trained a global XGBoost model evaluated using Root Mean Square Percentage Error (**RMSPE**).

---

## 📊 Results

**Evaluation Metric Formula:**

$$
\text{RMSPE} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} \left( \frac{y_i - \hat{y}_i}{y_i} \right)^2}
$$

| Model Configuration | Public Leaderboard RMSPE |
| :--- | :---: |
| Default XGBoost Regressor | 0.1235 |
| **XGBoost + Feature Engineering + Optuna Tuning** | **0.10385** |

---

## 📂 Project Structure

```text
.
├── data/                  # Raw dataset files
├── result/                # Output predictions and artifacts
├── latex-prezentacija/    # LaTeX source files for project presentation slides
├── latex-izvestaj/        # LaTeX source files for detailed research report
├── project.ipynb          # Main Jupyter Notebook (EDA, pipeline, Optuna & XGBoost)
└── README.md              # Project documentation
```

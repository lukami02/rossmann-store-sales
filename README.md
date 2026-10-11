📈 Rossmann Store Sales Forecasting

An end-to-end Machine Learning pipeline for predicting daily sales across 1,115 Rossmann drugstores using historical, promotional, and store-level data.

The project utilizes a highly tuned global XGBoost Regressor with hyperparameter optimization powered by Optuna, achieving an RMSPE of 0.10385 on the Kaggle public leaderboard.

🚀 Key Features

Data Preprocessing & Cleaning: Handled missing values, filtered closed store days, and formatted temporal data.

Feature Engineering: Built temporal/cyclical dynamics, promotional duration indicators, and lag/rolling statistics across store groups.

Hyperparameter Optimization: Used Optuna (Bayesian Optimization) to find optimal XGBoost parameters (max_depth, learning_rate, subsample, colsample_bytree, etc.).

Model: Global XGBoost model evaluated using Root Mean Square Percentage Error (RMSPE).

📊 Results

$$\text{RMSPE} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} \left( \frac{y_i - \hat{y}_i}{y_i} \right)^2}$$

Model Configuration

Public Leaderboard RMSPE

Default XGBoost Regressor

~0.1235

XGBoost + Feature Engineering + Optuna Tuning

0.10385

📂 Project Structure

├── data/                  # Raw dataset files
├── result/                # Output predictions
├── latex-prezentacija/    # LaTeX source files for project presentation slides
├── latex-izvestaj/        # LaTeX source files for detailed research report
├── project.ipynb          # Main Jupyter Notebook (EDA, pipeline, Optuna & XGBoost)
└── README.md              # Project documentation
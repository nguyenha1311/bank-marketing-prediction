# bank-marketing-prediction

## Overview

This project compares the performance of multiple supervised classification models on the [UCI Bank Marketing Dataset](https://archive.ics.uci.edu/ml/datasets/bank+marketing). The goal is to predict whether a client will subscribe to a term deposit (`y`) based on demographic, economic, and campaign-related features.

## Dataset

The dataset comes from direct marketing campaigns (phone calls) of a Portuguese banking institution. It contains **41,188 records** with **20 input features** including:

- **Client attributes:** age, job, marital status, education, credit default, housing/personal loans
- **Campaign attributes:** contact type, month/day of week, duration, number of contacts
- **Economic indicators:** employment variation rate, consumer price index, consumer confidence index, Euribor 3-month rate, number of employees

**Target variable:** `y` — whether the client subscribed to a term deposit (yes/no)

## Models Compared

The following classifiers were evaluated and compared:

| Model | Description |
|-------|-------------|
| **Logistic Regression** | Baseline linear classifier |
| **K-Nearest Neighbors (KNN)** | Instance-based learning |
| **Decision Tree** | Tree-based classifier |
| **Support Vector Machine (SVM)** | Margin-based classifier |

## Key Findings

- The dataset is **highly imbalanced** — the majority of clients did not subscribe, making accuracy alone an unreliable metric.
- **Logistic Regression** provides a strong baseline and is fast to train, offering good interpretability.
- **Decision Tree** models can overfit without proper pruning/hyperparameter tuning but provide clear feature importance rankings.
- **SVM** tends to perform well but at significantly higher computational cost on larger datasets.
- **KNN** performance is sensitive to the choice of `k` and feature scaling.
- Proper **feature engineering**, **encoding**, and **scaling** are critical preprocessing steps that impact all model performances.

## Notebook

📓 **[View the Jupyter Notebook](./prompt_III.ipynb)**

## Data Source
 
> [UCI Machine Learning Repository — Bank Marketing Dataset](https://archive.ics.uci.edu/ml/datasets/bank+marketing)

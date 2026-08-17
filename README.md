# Supply Chain Data Science Case Study

## Overview

This repository contains the data analysis supporting an RMIT Master of Data Science case study focused on the use of Data Science and machine learning in retail supply-chain management.

The analysis examines two public datasets from different parts of the supply chain and applies two machine-learning approaches to generate practical insights.

## Case Study

The analysis considers two supply-chain problems:

1. Predicting late-delivery risk using the DataCo Smart Supply Chain dataset.
2. Predicting Units Sold using the Retail Store Inventory Forecasting dataset.

The findings are used to consider how Data Science can support supply-chain decision-making.

## Machine Learning Models

### DataCo Smart Supply Chain

**Algorithm:** Logistic Regression

**Task:** Classification

**Target:** Late_delivery_risk

The model is evaluated using Accuracy, Precision, Recall, F1-score and ROC-AUC.

A decision-threshold analysis is also included to examine the trade-off between identifying late orders and generating false alerts.

### Retail Store Inventory Forecasting

**Algorithm:** Random Forest Regressor

**Task:** Regression

**Target:** Units Sold

The model is evaluated using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE) and R².

## Key Findings

- The DataCo Logistic Regression model identifies late-delivery risk with a ROC-AUC of approximately 0.745.
- Lowering the classification threshold increases recall from 54.3% to 77.8% and F1 from 67.3% to 71.3%, while reducing precision and accuracy.
- Shipping Mode shows a strong association with late-delivery outcomes in the DataCo dataset, although unusual patterns should not be directly generalised to real retail operations.
- Demand Forecast was excluded from the Retail model because its near-perfect correlation with Units Sold indicated a potential target-leakage issue.
- Inventory Level was the dominant feature in the Retail Random Forest model, with approximately 0.87 feature importance.
- The two datasets provide complementary perspectives on supply-chain management: fulfilment risk and inventory/demand behaviour.

## Repository Contents

```text
supply-chain-data-science-assignment/
│
├── README.md
├── part1_3_analysis.ipynb
├── model_results.csv
│
└── figures/
    ├── dataco_threshold.png
    ├── dataco_shipping_mode.png
    ├── retail_feature_importance.png
    └── retail_actual_vs_predicted.png

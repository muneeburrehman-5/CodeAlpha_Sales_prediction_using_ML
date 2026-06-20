# Advertising Sales Prediction & Impact Analysis

A Jupyter Notebook project for predicting sales from advertising spend using machine learning. The notebook explores how TV, Radio, and Newspaper advertising budgets influence sales and builds several regression models to forecast outcomes and compare performance.

## Project Overview

Organizations often struggle with:
- Uncertainty about ROI for each advertising channel
- Inefficient budget allocation across TV, Radio, and Newspaper
- Inability to forecast sales based on planned advertising spend
- Limited understanding of individual channel impact and synergy
- Lack of data-driven strategies for marketing optimization

This project addresses those challenges by:
- Cleaning and exploring the advertising dataset
- Engineering interaction and aggregate features
- Training multiple regression models
- Evaluating model performance
- Generating sales forecasts for different advertising scenarios

## Dataset

The notebook uses the classic **Advertising.csv** dataset, which contains:
- `TV`
- `Radio`
- `Newspaper`
- `Sales`

> Note: The notebook also contains an `Unnamed: 0` column, which appears to be an index column in the CSV.

## Methods Used

- Data loading and exploration
- Summary statistics and correlation analysis
- Outlier detection using IQR
- Feature engineering:
  - Interaction features
  - Total ad spend
  - Channel proportion features
- Standardization with `StandardScaler`
- Train/test split
- Model training:
  - Linear Regression
  - Ridge Regression
  - Lasso Regression
  - Random Forest Regressor
  - Gradient Boosting Regressor
- Cross-validation
- Scenario-based sales forecasting

## Model Performance

Based on the notebook output, the models performed as follows:

- **Linear Regression**: strong and interpretable baseline
- **Ridge Regression**: similar performance to linear regression
- **Lasso Regression**: slightly improved test performance
- **Random Forest**: very high training and test accuracy
- **Gradient Boosting**: best overall test performance in the notebook

## Key Findings

- **TV** has the strongest positive correlation with sales.
- **Radio** also has a meaningful positive effect.
- **Newspaper** has a weaker relationship with sales compared to TV and Radio.
- The combined advertising spend is strongly correlated with sales.
- Linear regression coefficients suggest:
  - TV has a positive impact
  - Radio has a stronger marginal impact than TV
  - Newspaper has a very small impact

## Forecast Scenarios

The notebook evaluates several advertising strategies, including:
- Conservative spend
- Balanced spend
- Aggressive spend
- TV-focused strategy
- Radio-focused strategy

These scenarios help estimate predicted sales and return on investment for different budget allocations.

## Requirements

Install the following Python libraries:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- warnings

You can install the main dependencies with:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn

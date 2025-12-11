# Strava Triathlon Race Time Predictor

A machine learning pipeline that analyzes Strava training data to predict triathlon race times.

## Overview

This project uses historical Strava activity data and past race results to build predictive models for triathlon performance. It includes two modeling approaches:

1. **Linear Regression Model** - Simple weighted training volume predictor
2. **XGBoost Model** - Advanced gradient boosting with engineered features

## Requirements

- Python 3.8+
- Jupyter Notebook or JupyterLab

## Installation

1. Clone or download this repository

2. Create a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Open either notebook:
   ```bash
   jupyter notebook linear_regression_model.ipynb
   # or
   jupyter notebook xgboost_model.ipynb
   ```

2. Run all cells - that's it!

The sample data is already included in the repo. Each notebook will automatically load its data and output performance metrics and visualizations.

## Features Engineered

The pipeline creates several features from training data:

- **Duration by sport** - Total swim/bike/run hours in training windows (30/60/90 days)
- **Weighted training volume** - Combined metric with sport-specific weights
- **Relative effort metrics** - Average, variance, and acute/chronic ratios
- **Training stress balance** - Acute (7-day) vs chronic (42-day) load comparison
- **Temporal features** - Day of week, month, time of year patterns

## Model Output

After running, you'll see:

- **RMSE/MAE** - Prediction error in seconds
- **Feature importance** - Which training metrics matter most
- **Visualizations** - Predicted vs actual plots, residual analysis

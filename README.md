# Crime Forecast XGBoost

Time series forecasting solution for predicting monthly crime incidents in Vancouver using machine learning. Achieves 84.7% variance explanation (R²) across 9 crime categories using XGBoost gradient boosting on 13 years of historical police data.

## Overview

- **Dataset**: 474,000+ crime incidents (Vancouver Police Department, 1999-2011)
- **Objective**: Monthly crime forecasting for 9 crime types
- **Evaluation Period**: 18 months (Jan 2012 - Jun 2013)
- **Best Model**: XGBoost (RMSE: 12.4 incidents/month, R²: 0.847)
- **Deployment**: Interactive Streamlit dashboard

## Project Structure

```
Crime-Forecast-XGBoost/
├── FBI_Crime_Investigation.ipynb    # Main notebook (127 cells)
├── app.py                           # Streamlit dashboard
├── requirements.txt                 # Dependencies
├── .streamlit/config.toml           # Streamlit configuration
├── xgb_final_model.joblib          # Trained XGBoost model
├── scaler.joblib                    # Feature scaler
├── label_encoder.joblib             # Categorical encoder
├── Test.csv                         # Test dataset
├── monthly_historical.csv           # Historical aggregates
├── hourly_crime_by_type.csv        # Hourly patterns
├── neighbourhood_crime.csv          # Geographic data
├── submission.csv                   # Predictions
└── README.md                        # This file
```

## Installation

```bash
git clone https://github.com/dhruvgaur10/Crime-Forecast-XGBoost.git
cd Crime-Forecast-XGBoost
pip install -r requirements.txt
```

## Usage

### Jupyter Notebook
```bash
jupyter notebook FBI_Crime_Investigation.ipynb
```

### Streamlit Dashboard
```bash
streamlit run app.py
```

Dashboard accessible at: `http://localhost:8501`

## Features

### Machine Learning Pipeline
- 15 exploratory visualizations (Univariate, Bivariate, Multivariate analysis)
- Feature engineering: temporal lags, rolling statistics, seasonal indicators
- Three model implementations: XGBoost, Random Forest, SARIMA
- Hyperparameter optimization using GridSearch and RandomSearch
- 5-fold cross-validation
- Feature importance analysis and model interpretability

### Interactive Dashboard
- Crime type selector with dynamic metric updates
- 7 interactive visualizations using Plotly and Mapbox
- Historical vs. forecast comparison chart
- Geographic hotspot mapping
- Monthly and hourly crime distribution analysis
- Exportable predictions in CSV format

## Model Performance

| Model | RMSE | MAE | R² Score |
|-------|------|-----|----------|
| XGBoost | 12.4 | 8.7 | 0.847 |
| Random Forest | 14.2 | 9.8 | 0.812 |
| SARIMA | 15.8 | 11.2 | 0.768 |

## Key Insights

1. Theft from Vehicle represents 32% of all crimes (153K incidents)
2. Summer months show 15-20% higher incident rates compared to winter
3. Property crimes concentrate during business hours (9am-5pm)
4. Central Business District accounts for 30% of all incidents
5. Previous month's crime count is the strongest predictor (35.2% feature importance)

## Technologies

- Python 3.8+
- XGBoost, Scikit-learn, Statsmodels
- Pandas, NumPy
- Matplotlib, Seaborn, Plotly
- GeoPandas, Mapbox
- Streamlit
- Joblib

## Running the Dashboard

```bash
streamlit run app.py
```

The dashboard will be accessible at `http://localhost:8501`

## Data Source

Vancouver Police Department historical crime records (1999-2011) publicly available under open data policies.

## Author

Dhruv Gaur

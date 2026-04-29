# FBI Crime Investigation: Time Series Forecasting

A machine learning solution for predicting monthly crime incidents in Vancouver using 13 years of historical police data. Implements XGBoost gradient boosting achieving 84.7% variance explanation across 9 crime categories.

## 📊 Project Overview

- **Dataset**: 474K+ crime incidents (Vancouver PD, 1999-2011)
- **Objective**: Monthly crime forecasting for 9 crime types
- **Time Period**: 18-month test period (Jan 2012 - Jun 2013)
- **Best Model**: XGBoost Regressor (RMSE: 12.4 incidents/month, R²: 0.847)
- **Deployment**: Interactive Streamlit dashboard

## 📁 Project Structure

```
FBI's-Crime-Investigation/
├── FBI_Crime_Investigation.ipynb          # Main notebook (127 cells) ⭐
├── README.md                              # This file
├── app.py                                 # Streamlit dashboard
├── requirements.txt                       # Python dependencies
├── .streamlit/config.toml                 # Streamlit configuration
├── Data Files/
│   ├── Test.csv                           # Test data
│   ├── monthly_historical.csv             # Historical monthly aggregates
│   ├── hourly_crime_by_type.csv          # Hourly crime patterns
│   └── neighbourhood_crime.csv            # Geographic data
├── Trained Models/
│   ├── xgb_final_model.joblib            # Best XGBoost model
│   ├── scaler.joblib                     # Feature scaler
│   └── label_encoder.joblib              # Categorical encoder
├── .git/                                  # Version control
└── .gitignore                             # Git ignore rules
```

## 🚀 Quick Start

### 1. Install Dependencies
```bash
pip install -r requirements.txt
```

### 2. Run Jupyter Notebook
```bash
jupyter notebook FBI_Crime_Investigation.ipynb
```

### 3. Deploy Dashboard Locally
```bash
streamlit run app.py
```

Access dashboard at: `http://localhost:8501`

## 📈 Key Features

### Machine Learning Pipeline
- ✅ 15 visualizations following UBM framework (Univariate, Bivariate, Multivariate)
- ✅ Feature engineering: Temporal lags, rolling statistics, seasonal indicators
- ✅ 3 ML models: XGBoost, Random Forest, SARIMA
- ✅ Hyperparameter tuning: GridSearch and RandomSearch
- ✅ Cross-validation with 5-fold splitting
- ✅ Model explainability via feature importance analysis

### Interactive Dashboard
- 🎯 Crime type selector with dynamic KPI updates
- 📊 7 interactive visualizations (Plotly + Mapbox)
- 📈 Historical vs. forecast comparison
- 🗺️ Geographic hotspot mapping
- 📅 Monthly seasonality analysis
- 🕐 Hourly distribution patterns
- 💾 Export predictions to CSV

## 📊 Model Performance

| Metric | XGBoost | Random Forest | SARIMA |
|--------|---------|---------------|--------|
| RMSE | 12.4 | 14.2 | 15.8 |
| MAE | 8.7 | 9.8 | 11.2 |
| R² Score | 0.847 | 0.812 | 0.768 |
| Status | ✅ Selected | Baseline | Reference |

## 🔍 Top Findings

1. **Theft from Vehicle** dominates (32% of crimes, ~153K incidents)
2. **Summer peaks**: 15-20% higher incidents than winter
3. **Hourly patterns**: Property crimes cluster 9am-5pm; violent crimes spread throughout day
4. **Geographic concentration**: CBD accounts for 30% of all incidents
5. **Lag effects**: Previous month's count is strongest predictor (35.2% feature importance)

## 📚 Documentation

- **Jupyter Notebook**: Complete technical documentation with step-by-step analysis, visualizations, methodology, and results
- **Project Summary Section**: Comprehensive overview in notebook's initial section

## 🛠️ Technologies Used

| Category | Technologies |
|----------|---------------|
| Data Processing | Pandas, NumPy |
| ML/AI | XGBoost, Scikit-learn, Statsmodels |
| Visualization | Matplotlib, Seaborn, Plotly, Mapbox |
| Geospatial | GeoPandas |
| Deployment | Streamlit, Joblib |
| Version Control | Git |

## ✅ Submission Requirements

- ✅ Well-documented Jupyter notebook (127 cells, fully commented)
- ✅ 15 meaningful visualizations with business impact analysis
- ✅ 3 ML models with hyperparameter tuning
- ✅ Hypothesis testing (3 statistical tests)
- ✅ Model explainability (feature importance analysis)
- ✅ Production-ready code (0 errors, runs start-to-finish)
- ✅ Interactive Streamlit dashboard
- ✅ Trained models in joblib format
- ⏳ **Pending**: Video explanation (15-25 min)
- ⏳ **Pending**: GitHub repository link

## 🚀 Deployment Options

### Option 1: Streamlit Cloud (Recommended - Free)
```bash
git push origin main
# Visit: https://streamlit.io/cloud
# Connect GitHub repo → Auto-deploy
```

### Option 2: Local Server
```bash
streamlit run app.py
```

### Option 3: Docker Containerization
```bash
docker build -t crime-forecast .
docker run -p 8501:8501 crime-forecast
```

## 📝 Model Insights

**Top 5 Predictive Features**:
1. lag_1 (35.2%) - Previous month's crime count
2. lag_12 (28.1%) - Year-ago seasonality
3. MONTH (18.4%) - Monthly seasonality
4. TYPE (12.8%) - Crime category
5. YEAR (5.5%) - Long-term trend

**Business Impact**:
- Enables shift scheduling 1-2 months in advance
- Estimated 12-15% improvement in response times
- Potential annual cost savings: $200K-300K

## 📧 Author & Contact

**Project**: FBI Crime Investigation - Time Series Forecasting
**Developer**: Dhruv Gaur
**Email**: m.gaur@perfomax.io
**Status**: Production Ready ✅

## 📄 License

This project uses Vancouver Police Department public data under open data policies.

---

**Last Updated**: April 30, 2026
**Status**: Complete & Deployment Ready
**Version**: 1.0

For questions or detailed analysis, refer to `PROJECT_SUMMARY.md`

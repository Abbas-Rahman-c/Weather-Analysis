# 🌍 Global Weather Trend Forecasting

**Author:** Abbas Rahman  
**Assessment:** Advanced Data Science — PM Accelerator  
**Dataset:** [Global Weather Repository — Kaggle](https://www.kaggle.com/datasets/nelgiriyewithana/global-weather-repository)

---

## 📌 Project Overview

This project performs a comprehensive analysis and forecasting of global daily weather data. It covers the full data science pipeline — from cleaning and exploratory analysis through to multi-model forecasting, ensemble stacking, and geospatial visualization.

---

## 📂 Contents

| File | Description |
|---|---|
| `Data_Science_Assessment.ipynb` | Main analysis notebook |
| `GlobalWeatherRepository.csv` | Source dataset (download from Kaggle) |
| `fig_*.png` | Generated visualizations |
| `fig_climate_trends.html` | Interactive climate trend chart |
| `fig_geo_map.html` | Interactive global temperature map |

---

## 🔬 Analysis Sections

1. **Data Loading & Inspection** — Shape, column types, null summary
2. **Data Cleaning & Preprocessing** — Datetime parsing, missing value imputation, IQR outlier removal, MinMax normalization
3. **Advanced EDA** — Isolation Forest anomaly detection, correlation heatmap, seasonal decomposition, ADF & KPSS stationarity tests
4. **Forecasting Models** — Four models trained and evaluated on global daily mean temperature:
   - SARIMA
   - Facebook Prophet
   - XGBoost (with lag features)
   - LSTM (deep learning)
5. **Ensemble Model** — Weighted average stacking using inverse-RMSE weights
6. **Climate Analysis** — Monthly trends by country, seasonal boxplots
7. **Environmental Impact** — AQI & air quality correlation with weather variables
8. **Feature Importance (SHAP)** — Bar and beeswarm plots from XGBoost
9. **Spatial Analysis** — Interactive global temperature map, warmest/coldest countries chart
10. **Key Insights & Conclusions** — Final model comparison and findings

---

## 📊 Models & Metrics

All models are evaluated on an 80/20 time-based train/test split using:
- **MAE** (Mean Absolute Error)
- **RMSE** (Root Mean Squared Error)
- **R²** (Coefficient of Determination)

The **Ensemble model** (inverse-RMSE weighted average) achieves the best overall performance.

---

## 🛠️ Requirements

Install dependencies with:

```bash
pip install numpy pandas matplotlib seaborn plotly scikit-learn xgboost shap statsmodels prophet tensorflow folium scipy
```

> **Note:** TensorFlow and Prophet may require additional setup depending on your OS. Python 3.8+ is recommended.

---

## 🚀 How to Run

1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/nelgiriyewithana/global-weather-repository) and place `GlobalWeatherRepository.csv` in the same directory as the notebook.
2. Open `Data_Science_Assessment.ipynb` in Jupyter or Google Colab.
3. Run all cells in order (`Runtime → Run all` in Colab).

---

## 💡 Key Findings

- Isolation Forest flagged ~5% of records as anomalies, mostly extreme readings at polar and desert stations.
- Strong annual and weekly seasonality confirmed via decomposition.
- Recent lag features (1-day, 7-day) are the strongest temperature predictors according to SHAP.
- Equatorial regions show consistently high temperatures; the Northern Hemisphere shows the strongest seasonal swings.
- The Ensemble model outperformed all individual forecasting models.

---

## 🏢 About PM Accelerator

> PM Accelerator empowers aspiring and experienced product managers with the tools, community, and real-world experience needed to accelerate their careers. Through mentorship, hands-on projects, and industry connections, we bridge the gap between ambition and achievement.

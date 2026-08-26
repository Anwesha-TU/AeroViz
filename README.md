# AeroViz 🌫️✈️

## AI-Based Visibility Prediction and Forecasting Using Atmospheric and Air Quality Data

AeroViz is a machine learning and deep learning-based project for predicting and forecasting atmospheric visibility at IGI Airport using meteorological and air-quality parameters.

The project investigates the relationship between visibility and atmospheric conditions, including **PM₂.₅, relative humidity, temperature, wind speed, and boundary layer height (BLH)**. It compares models based on local airport observations with models incorporating atmospheric information from the wider Delhi region.

In addition to same-time visibility prediction, AeroViz performs short-term visibility forecasting at **1-hour, 3-hour, and 6-hour lead times**, using atmospheric conditions available at the forecast issue time to predict future visibility.

---

## 📌 Objectives

The main objectives of AeroViz are to:

- Analyze the relationship between meteorological conditions, particulate pollution, and atmospheric visibility.
- Investigate seasonal and temporal variations in low-visibility and fog events.
- Perform Pearson correlation and moving-window correlation analysis between visibility and atmospheric variables.
- Develop and compare machine learning models for same-time visibility prediction.
- Compare two different training strategies:
  - **Case 1:** Training using fog-prone months.
  - **Case 2:** Training using the full available training period.
- Compare model performance using:
  - **Airport-specific atmospheric data.**
  - **Regional atmospheric data from multiple stations across Delhi, while predicting visibility at IGI Airport.**
- Evaluate model performance for predicting fog events and different fog severity categories:
  - **Shallow Fog:** 700–1000 m
  - **Dense Fog:** 350–700 m
  - **Very Dense Fog:** <350 m
- Develop short-term visibility forecasting models for:
  - **1-hour lead time**
  - **3-hour lead time**
  - **6-hour lead time**
- Investigate how forecasting performance changes with increasing lead time.
- Compare the effect of fog-season-specific training and full-period training on short-term visibility forecasting.
- Develop and compare deep learning models for visibility prediction and forecasting.

---

## 🌫️ Problem Statement

Low visibility is a significant atmospheric phenomenon, particularly during the winter months over the Indo-Gangetic Plain (IGP). Visibility can be influenced by aerosol loading, relative humidity, meteorological conditions, boundary-layer dynamics, and other atmospheric processes.

This project uses observational and reanalysis data to develop data-driven models for predicting current visibility and forecasting future visibility at IGI Airport.

The project addresses two related problems.

### 1. Same-Time Visibility Prediction

Atmospheric and air-quality conditions observed at time \(t\) are used to predict visibility at the same time:

```text
Atmospheric and Air Quality Variables at time t
                    ↓
          Machine Learning /
           Deep Learning Model
                    ↓
        Predicted Visibility at time t
```

### 2. Short-Term Visibility Forecasting

Atmospheric and air-quality conditions available at the forecast issue time are used to predict future visibility:

Forecast Issue Time (t)
        │
        │ Atmospheric and air-quality observations
        │
        ├──► Forecast visibility at t + 1 hour
        │
        ├──► Forecast visibility at t + 3 hours
        │
        └──► Forecast visibility at t + 6 hours

🤖 Machine Learning Models

The machine learning models investigated include:

- Linear Regression
- Ridge Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- Support Vector Regression (SVR)

Deep learning models are also investigated as part of the project.

📊 Model Evaluation
Visibility Prediction and Forecasting

Regression performance is evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- Coefficient of Determination (R²)
- Fog Event Detection

Predicted and observed visibility values are also evaluated for their ability to identify fog events using metrics such as:

- Probability of Detection (POD)
- False Alarm Ratio (FAR)
- Critical Success Index (CSI)
- Precision
- Recall
- F1 Score
- Fog Severity Classification

Fog events are further divided into three severity categories:

- Shallow Fog	700–1000 m
- Dense Fog	350–700 m
- Very Dense Fog	<350 m

Model predictions are evaluated to determine how accurately fog events are assigned to the correct severity category and whether models tend to underestimate or overestimate fog severity.

📁 Data Sources and Input Variables

The project combines atmospheric, meteorological, air-quality, and visibility data.

The primary variables investigated include: PM₂.₅, Relative Humidity (RH), Temperature, Wind Speed, Boundary Layer Height (BLH) and Visibility

For the regional-data experiments, atmospheric and air-quality information from multiple stations across the Delhi region is incorporated while the prediction target remains visibility at IGI Airport.

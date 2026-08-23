# AeroViz 🌫️✈️

## AI-Based Visibility Prediction Using Atmospheric and Air Quality Data at various stations

AeroViz is a machine learning and deep learning project focused on predicting atmospheric visibility at various stations, using meteorological and air-quality parameters.

The project investigates the relationship between visibility and atmospheric conditions: **PM₂.₅, relative humidity, temperature, wind speed, and boundary layer height (BLH)**. It also compares predictions based on local airport observations with those based on atmospheric information from the wider Delhi region.

---

## 📌 Project Objectives

The main objectives of AeroViz are to:

- Analyze the relationship between meteorological conditions, particulate pollution, and atmospheric visibility.
- Investigate seasonal and temporal variations in low-visibility events.
- Perform correlation and moving-window correlation analysis between visibility and atmospheric variables.
- Develop machine learning models for visibility prediction.
- Compare two different training strategies.
- Compare prediction performance using:
  - Airport-specific data.
  - Regional data from multiple stations.
- Develop and compare deep learning models for visibility prediction.

---

## 🌫️ Problem Statement

Low visibility is a significant atmospheric phenomenon, particularly during the winter months over the Indo-Gangetic Plain (IGP). Visibility can be influenced by aerosol loading, relative humidity, meteorological conditions, boundary-layer dynamics, and other atmospheric processes.

This project uses observational and reanalysis data to develop data-driven models capable of predicting visibility at various stations

The central prediction problem can be represented as:

```text
Atmospheric and Air Quality Variables
                ↓
        Machine Learning /
         Deep Learning
                ↓
      Predicted Visibility

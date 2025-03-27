# TwIn Solar - Improving Research and Innovation in Solar Renewables

## Overview
This project evaluates the potential of machine learning tools for analyzing and forecasting load patterns and PV production in a smart microgrid system. The dataset provided by the University of La Reunion was used for this analysis.

## Objectives
- Forecast load patterns and PV production using historical data.
- Analyze the impact of weather parameters on PV production.
- Calculate the energy gap between load requirements and PV production.

## Background
The TwIn Solar project aims to revolutionize solar energy integration through advanced machine learning capabilities. This study focuses on the University of La Reunion, located on a tropical island where variable weather conditions significantly impact solar energy production.

## Methodology
1. **Data Collection**:
   - Historical PV production data from campus buildings.
   - Weather data including Global Horizontal Irradiance (GHI), Beam Normal Irradiance (BNI), Diffuse Horizontal Irradiance (DHI), temperature, humidity, wind speed, etc.

2. **Data Preprocessing**:
   - Handling missing values using interpolation and forward/backward fill.
   - Outlier detection and treatment using Interquartile Range (IQR).
   - Feature engineering: Hour of the day, day of the week, month of the year, lagged PV production values.
   - Normalization using MinMaxScaler.

3. **Model Development**:
   - Baseline models: Simple Linear Regression.
   - Advanced models: LSTM networks with and without weather data.
   - Evaluation metrics: Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), R-squared (R²).

4. **Cloud Infrastructure**:
   - Microsoft Azure for data storage and processing.
   - Azure Databricks with Apache Spark for efficient data preparation and transformation.

## Results
- **Without Weather Data**:
  - RMSE: Dpt 1 2 = 0.4804, ENERPOS = 2.0462, ESIROI = 5.5377.
  - MAE: Dpt 1 2 = 0.2031, ENERPOS = 0.9322, ESIROI = 2.8015.

- **With Weather Data**:
  - RMSE: Dpt 1 2 = 0.46, ENERPOS = 1.94, ESIROI = 3.33.
  - MAE: Dpt 1 2 = 0.19, ENERPOS = 0.87, ESIROI = 1.24.

- **Key Insights**:
  - Incorporating weather data significantly improves forecast accuracy.
  - Global Horizontal Irradiance (GHI) has the highest influence on PV production.

## Dependencies
- Python 3.x
- Libraries: pandas, numpy, matplotlib, scikit-learn, TensorFlow/Keras, PVLib
- Cloud Services: Microsoft Azure, Azure Databricks

## Instructions to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/TwInSolar-Project.git
# TwIn Solar – Improving Research and Innovation in Solar Renewables

## Overview
This project evaluates the potential of machine learning tools for analyzing and forecasting load patterns and photovoltaic (PV) production in a smart microgrid system.  
The dataset provided by the **University of La Réunion** was used for this analysis.

## Objectives
- Forecast load patterns and PV production using historical data.  
- Analyze the impact of weather parameters on PV production.  
- Calculate the energy gap between load requirements and PV production.  
- Explore the use of **cloud-based infrastructure (Azure)** for scalable data preparation and experimentation.

## Background
The TwIn Solar project aims to advance solar energy integration through modern data science techniques.  
This study focuses on the University of La Réunion, located on a tropical island where variable weather conditions significantly affect solar energy production.

## Methodology
1. **Data Collection**
   - Historical PV production data from campus buildings.  
   - Weather data including Global Horizontal Irradiance (GHI), Beam Normal Irradiance (BNI), Diffuse Horizontal Irradiance (DHI), temperature, humidity, and wind speed.

2. **Data Preprocessing**
   - Missing value handling using interpolation and forward/backward fill.  
   - Outlier detection and treatment with the Interquartile Range (IQR) method.  
   - Feature engineering: hour of day, day of week, month of year, lagged PV production values.  
   - Normalization using MinMaxScaler.

3. **Model Development**
   - Baseline models: Simple Linear Regression.  
   - Advanced models: LSTM networks with and without weather features.  
   - Evaluation metrics: Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and R-squared (R²).

4. **Cloud Infrastructure**
   - **Microsoft Azure** was used to store and process the dataset.  
   - **Azure Databricks** (Apache Spark environment) provided a collaborative workspace for exploratory analysis, feature engineering, and model training at scale.  
   - Notebooks were executed in Databricks clusters for efficient transformations and reproducibility.

## Results
- **Without Weather Data**  
  - RMSE: Dpt 1 2 = 0.4804, ENERPOS = 2.0462, ESIROI = 5.5377  
  - MAE: Dpt 1 2 = 0.2031, ENERPOS = 0.9322, ESIROI = 2.8015
- **With Weather Data**  
  - RMSE: Dpt 1 2 = 0.46, ENERPOS = 1.94, ESIROI = 3.33  
  - MAE: Dpt 1 2 = 0.19, ENERPOS = 0.87, ESIROI = 1.24
- **Key Insights**
  - Incorporating weather data significantly improves forecast accuracy.  
  - Global Horizontal Irradiance (GHI) is the most influential parameter for PV production.

## Dependencies
- Python 3.x  
- Libraries: `pandas`, `numpy`, `matplotlib`, `scikit-learn`, `tensorflow`/`keras`, `pvlib`  
- Cloud Services: **Microsoft Azure**, **Azure Databricks**

## Instructions to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/vk20001/TwinSolar--.git
   ```
2. Follow the notebooks for data preprocessing, model training, and evaluation.  
3. (Optional) To replicate the cloud workflow, upload the data to Azure Blob Storage and run the notebooks inside an Azure Databricks workspace.

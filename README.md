# Forecasting-Order-Completion


# Sales Forecasting with ARIMA

This repository contains the implementation of a sales forecasting model using the ARIMA (AutoRegressive Integrated Moving Average) method. The model is trained on historical sales data and used to predict future sales for a given time period.

## Project Overview

The goal of this project is to forecast future sales using ARIMA, following the steps below:

1. **Data Preprocessing:**
   - The historical sales data is checked for stationarity using the Augmented Dickey-Fuller (ADF) test.
   - In case of non-stationarity, the first-order difference is applied to make the data stationary.
   
2. **Stationarity Check:**
   - The stationarity of the data is validated using the ADF and Kolmogorov-Smirnov (KS) tests.

3. **Model Selection:**
   - The Autocorrelation Function (ACF) and Partial Autocorrelation Function (PACF) are plotted to determine the optimal values of the AR (p) and MA (q) terms for the ARIMA model.

4. **ARIMA Model:**
   - The ARIMA model with parameters (2,1,2) is selected based on ACF/PACF analysis.
   - The model is trained on 90% of the historical data.

5. **Model Evaluation:**
   - The model's performance is evaluated using the Mean Absolute Percentage Error (MAPE), which achieved a value of 20% on the training data.

6. **Prediction:**
   - The trained ARIMA model is then used to predict sales for the next 30 days.

## Files

- `data.csv`: Historical sales data used for forecasting.
- `Forecasting order completion-checkpoint.ipynb`: Script implementing the ARIMA model, including data preprocessing, model training, and prediction.

## Installation

To run this project, clone the repository and install the required dependencies:

bash :
git clone https://github.com/MukulGoel25/Forecasting-Order-Completion

pip install -r requirements.txt


## Requirements

- Python 3.7+
- pandas
- numpy
- matplotlib
- statsmodels
- scipy

## Usage

1. Download the sales data and save it as `data.csv`.
2. Run the script to preprocess the data and train the ARIMA model
3. The script will output the predicted sales for the next 30 days and display the performance evaluation metrics.

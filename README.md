Bitcoin Price Prediction
Overview
This Jupyter notebook (bitcoin_price_prediction.ipynb) is designed for predicting Bitcoin prices using historical data. It includes data preprocessing, feature engineering, and model implementation to forecast future Bitcoin prices.
Dependencies
The notebook requires the following Python packages, which are installed in the environment:

pmdarima: For time series forecasting using ARIMA models.
pandas: For data manipulation and analysis.
numpy: For numerical computations.
scikit-learn: For machine learning utilities.
scipy: For scientific and technical computing.
statsmodels: For statistical modeling.
cython, joblib, patsy, python-dateutil, pytz, python-tzdata, threadpoolctl: Supporting libraries for efficient computation and data handling.
libopenblas, libblas, libcblas, liblapack, libgfortran, libgfortran5: Linear algebra libraries for optimized numerical operations.
ca-certificates, certifi, conda, openssl: For environment and security management.

These dependencies are installed via conda from the conda-forge channel, as shown in the notebook's first cell.
Dataset
The notebook uses a dataset containing Bitcoin price data, stored in a pandas DataFrame (df_valid). The dataset includes the following key columns:

Timestamp: Date of the price data (e.g., 2023-01-01 to 2025-06-09).
Open, High, Low, Close: Daily Bitcoin price metrics.
Volume_(Currency): Trading volume in currency.
Feature-engineered columns:
Lagged means and standard deviations for Open, High, Low, Close, and Volume_(Currency) over 3 and 30 days (e.g., Open_mean_lag3, Open_std_lag3, Close_mean_lag30, etc.).
Temporal features: month, week, day, day_of_week.


The dataset spans 891 rows, covering daily data from January 1, 2023, to June 9, 2025.

Usage

Environment Setup:

Ensure the required dependencies are installed using the conda command provided in the notebook.
Run the notebook in a Jupyter environment (e.g., Google Colab, as indicated by the metadata).


Data Exploration:

The notebook displays the df_valid DataFrame, which contains the processed Bitcoin price data with feature-engineered columns.


Modeling:

The notebook is set up for time series forecasting, likely using the pmdarima library for ARIMA-based models (though the specific modeling code is not shown in the provided snippet).
Users can extend the notebook by adding model training and evaluation steps.


Execution:

Run the cells sequentially to install dependencies and load the dataset.
The final cell displays the df_valid DataFrame for inspection.



Notes

The notebook is tailored for Google Colab, as indicated by the colab metadata and interactive DataFrame visualization code.
The dataset includes future dates (up to June 2025), suggesting it may contain simulated or forecasted data for testing purposes.
Ensure you have sufficient computational resources, as the dataset and dependencies (e.g., libopenblas, scipy) are computationally intensive.

Requirements

Python 3.x
Jupyter Notebook or Google Colab
Internet access for downloading dependencies via conda

Contributing
Feel free to fork this project, add improvements (e.g., additional models, visualizations, or feature engineering), and submit pull requests.
License
This project is unlicensed. Use it at your own discretion.

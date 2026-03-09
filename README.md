⚡ U.S. Lower 48 Electricity Demand Forecasting

Machine learning project predicting hourly electricity demand across the U.S. Lower 48 using time-series modeling and ensemble regression techniques.

📌 Project Overview

Electricity demand fluctuates throughout the day and across seasons due to human activity patterns, weather conditions, and energy generation dynamics. Accurate demand forecasting is essential for maintaining grid reliability, minimizing operational costs, and optimizing energy generation.

This project builds and evaluates machine learning models to forecast hourly electricity demand using historical generation data and engineered time-based features.

The final model achieves 94.4% explained variance (R² = 0.944) using a Random Forest Regressor.

🎯 Problem Statement

Power grid operators must balance supply and demand in real time. Poor demand forecasting can lead to:

Overproduction and unnecessary costs

Underproduction and grid instability

Inefficient energy dispatch

The goal of this project is to develop a predictive model capable of accurately forecasting hourly electricity demand (MW) based on generation source data and temporal patterns.

📊 Dataset

The dataset contains hourly observations of electricity demand across the U.S. Lower 48, including:

Target Variable

demand_mw — total electricity demand in megawatts

Generation Features

coal_mw

gas_mw

nuclear_mw

hydro_mw

solar_mw

wind_mw

petroleum_mw

other_mw

Time Feature

datetime

🧹 Data Preparation

The following preprocessing steps were applied:

Chronological sorting of time-series data

Feature engineering from datetime:

Hour of day

Day of week

Month

Weekend indicator

Chronological 80/20 train-test split

TimeSeriesSplit cross-validation

Model evaluation using regression metrics

Because this is a time-series forecasting problem, random train-test splitting was avoided to prevent data leakage.

🤖 Models Evaluated

Three regression models were trained and compared:

Model	Description
Linear Regression	Baseline linear model
Random Forest	Ensemble tree-based model capturing nonlinear relationships
Gradient Boosting	Sequential boosting ensemble model
📈 Model Performance
Model	MAE	RMSE	R²
Linear Regression	21,538	27,135	0.841
Random Forest	12,286	16,104	0.944
Gradient Boosting	14,398	18,573	0.926

Random Forest produced the lowest prediction errors and highest R² score, making it the best model for this project.

📊 Visualizations
Electricity Demand Over Time

Model Performance Comparison

Actual vs Predicted Electricity Demand

🏆 Final Model

The Random Forest Regressor was selected as the final model due to:

Highest R² score (0.944)

Lowest MAE and RMSE

Strong ability to capture nonlinear demand patterns

This model provides reliable short-term electricity demand forecasting.

📂 Repository Structure
capstone-two-electricity-demand
│
├── notebooks
│   ├── Capstone_Two_Preprocessing.ipynb
│   ├── Capstone_Two_Modeling.ipynb
│
├── visuals
│   ├── demand_over_time.png
│   ├── model_comparison.png
│   ├── actual_vs_predicted.png
│
├── model_metrics.csv
├── Capstone_Final_Report.pdf
├── README.md
🚀 Technologies Used

Python

Pandas

NumPy

Scikit-learn

Matplotlib

Jupyter Notebook

🔮 Future Improvements

Potential enhancements for this project include:

Incorporating weather and temperature data

Adding lag features for autoregressive forecasting

Hyperparameter tuning using TimeSeriesSplit

Testing advanced models such as XGBoost or LightGBM

📚 Project Author

Justin Ali
Springboard Data Science Career Track

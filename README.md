# new-york-taxi-trips
NYC Taxi Tip Prediction & Analysis
Project Overview: This project performs an end-to-end analysis of NYC Yellow Taxi data to predict tip amounts. It demonstrates a complete data pipeline from cloud-based sourcing to predictive modeling, with a strong focus on Data Validation and Model Optimization.
Tech StackCloud: Google BigQueryLanguage: Python (Pandas, NumPy)Visualization: Seaborn, Matplotlib
Machine Learning: Scikit-Learn (Linear Regression, Random Forest, Gradient Boosting) 
Key Phases: Data Sourcing: Extracted 10k+ records from BigQuery public datasets.
Verification & Cleaning: Removed negative fares and zero-distance trips. Handled data type mismatches (Object to Float conversion).
Feature Engineering: Extracted hour_of_day, day_of_week, and is_rush_hour from raw timestamps to capture temporal patterns.
Exploratory Data Analysis (EDA): Identified peak tipping hours (4 AM - 6 AM) using Heatmaps, correlating them with airport commutes and business travel patterns.
Predictive Modeling: Compared three different algorithms:Linear Regression: Achieved the best baseline (R^2=0.16).
Random Forest & GB: Analyzed performance drops due to overfitting and low signal-to-noise ratio in the features provided.
Results & Insights By performing Outlier Removal (95th percentile), I successfully reduced the Mean Squared Error (MSE) by 73%, creating a more robust and reliable model for typical urban trips.

# NYC Taxi Tip Prediction & Analysis

## Project Overview
This project executes a full-cycle data science pipeline to predict taxi tip amounts in New York City. By leveraging NYC Yellow Taxi public datasets, the analysis demonstrates a complete workflow from cloud-based data sourcing to advanced predictive modeling, with a heavy emphasis on data integrity and hyperparameter optimization.

---

## Key Phases

### 1. Data Sourcing & Infrastructure
* **Cloud Integration:** Extracted and queried over 10,000 records directly from **Google BigQuery** public datasets.
* **Tech Stack:** Processed using **Python (Pandas, NumPy)** and visualized via **Seaborn/Matplotlib**.

### 2. Verification & Cleaning (Data Quality)
* **Outlier Removal:** Identified and eliminated negative fares and zero-distance "ghost" trips.
* **Type Conversion:** Resolved data type mismatches (Object to Float) to ensure mathematical consistency.
* **Robustness:** Applied 95th percentile outlier removal, which successfully **reduced Mean Squared Error (MSE) by 73%**.

### 3. Feature Engineering & EDA
* **Temporal Patterns:** Engineered new features including `hour_of_day`, `day_of_week`, and `is_rush_hour` from raw timestamps.
* **Behavioral Insights:** Used **Heatmaps** to identify peak tipping windows (4 AM - 6 AM), correlating high gratuities with airport commutes and early business travel.

---

## Predictive Modeling
Compared three distinct algorithms to find the optimal balance between bias and variance:

| Algorithm | Result / Insight |
| :--- | :--- |
| **Linear Regression** | Achieved the best baseline performance with an **$R^2 = 0.16$**. |
| **Random Forest** | Analyzed performance drops caused by a low signal-to-noise ratio in specific features. |
| **Gradient Boosting** | Evaluated for non-linear patterns; utilized to study potential overfitting risks. |

---

## Key Results & Insights
* **Model Optimization:** The strategic removal of extreme outliers transformed the model from high-variance to a robust tool for typical urban trips.
* **Business Value:** Identified that "Time of Day" is a critical predictor for tip percentage, allowing for better revenue forecasting based on shift timing.

---

## Project Structure
* `data_sourcing.sql` - BigQuery extraction scripts.
* `eda_visualizations.ipynb` - Heatmaps and distribution analysis.
* `model_training.py` - Scikit-Learn pipeline and evaluation.

---
**Developed by Safaa Tareef Hasan**

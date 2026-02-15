# stranger_things
#Model Performance &amp; Evaluation
# Flight Fare Prediction & Regression Analysis

## Project Overview
This project focuses on predicting airline ticket fares using a dataset of over **10,000 records**. It demonstrates a robust end-to-end machine learning pipeline, moving from raw, unstructured string data to high-performance predictive models. The project compares traditional ensemble methods against deep learning architectures to identify the most effective solution for right-skewed financial data.

## Technical Workflow

### 1. Data Engineering & Cleaning
Real-world flight data is notoriously messy. I implemented custom logic to handle these specific challenges:
* **String Parsing**: Created an automated script to handle inconsistent datetime formats (e.g., "12:35" vs "19:00 22 May").
* **Feature Extraction**: Derived high-value temporal features including `Journey_Day`, `Journey_Month`, `Dep_Hour`, and converted raw text durations into a numerical `Total_Duration_Minutes`.
* **Missing Value Handling**: Identified and managed null values in critical columns like 'Route' and 'Total_Stops'.

### 2. Exploratory Data Analysis (EDA)
* **Price Distribution**: Conducted statistical analysis identifying a significant right-skew in ticket prices, informing the decision to use models robust to outliers.
* **Feature Correlation**: Analyzed the relationship between flight duration, total stops, and the final ticket price.

### 3. Machine Learning & Deep Learning Modeling
I compared three distinct approaches to optimize predictive accuracy:
* **XGBoost Regressor**: Utilized gradient boosting to capture non-linear relationships in the tabular data.
* **Random Forest Regressor**: Implemented an ensemble of decision trees to provide a stable, high-performance baseline.
* **Neural Network (Keras/TensorFlow)**: Developed a **Sequential Deep Learning** model to explore the efficacy of neural architectures on regression tasks.


## Model Performance & Evaluation
Models were evaluated using a multi-metric approach to ensure business-level accuracy:
* **Primary Metrics**: $R^2$ Score, RMSE (Root Mean Square Error), and MAPE (Mean Absolute Percentage Error).
* **Visualization**: Utilized dual-axis line plots to compare divergent metrics (high-scale RMSE vs. 0-1 scale $R^2$) across all models.

## Technologies Used
* **Languages**: Python
* **ML/DL Frameworks**: Scikit-learn, XGBoost, TensorFlow, Keras
* **Data Ops**: Pandas, NumPy
* **Visualization**: Seaborn, Matplotlib

## Key Takeaways
* **Ensemble methods** (XGBoost/Random Forest) provided the most reliable predictions for this specific dataset.
* **Feature Engineering** of temporal data was the single biggest driver of model performance improvement.

---
*Developed as part of the Master's program at the University of North Texas*.

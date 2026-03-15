Cardiovascular Disease Prediction
Project Overview
This project aims to predict the presence or absence of cardiovascular disease based on various patient parameters. Machine learning models, including Logistic Regression, Random Forest, and XGBoost, were trained and evaluated. Explainable AI techniques (SHAP) were used to interpret model predictions and identify key contributing factors.

Dataset
The dataset used in this project is cardiac_failure_processed.csv, which contains patient health metrics. The dataset was cleaned by removing the 'id' column, converting age from days to years, and calculating the Body Mass Index (BMI).

Methods
Data Loading & Exploration: The dataset was loaded, and initial exploratory data analysis was performed, including checking data types, descriptive statistics, and missing values. Visualizations like age distribution, cardiovascular disease counts, and a feature correlation heatmap were generated.
Data Preprocessing: Features (X) and target (y) were defined. The dataset was split into training and testing sets (80/20 split).
Model Training: Three classification models were trained:
Logistic Regression
Random Forest Classifier
XGBoost Classifier
Model Evaluation: Each model's performance was evaluated using accuracy scores. The best-performing model (XGBoost) was further assessed using a confusion matrix and a classification report.
Feature Importance & Explainable AI: Feature importances from the Random Forest model were visualized. SHAP (SHapley Additive exPlanations) values were used with the XGBoost model to understand individual feature contributions to predictions.
Prediction Function & Model Saving: A Python function predict_risk was created to make predictions on new data, and the trained XGBoost model was saved using joblib.
Results
Model Performance: XGBoost demonstrated the highest accuracy among the trained models, achieving approximately 73.49% accuracy.
Key Features: The feature importance and SHAP analysis identified several critical factors influencing cardiovascular disease risk, such as age, ap_hi, ap_lo, and weight.
Model Interpretability: SHAP plots provided insights into how individual feature values positively or negatively impact the prediction of cardiovascular disease.
Future Work
Hyperparameter Tuning: Further optimize model performance by rigorously tuning hyperparameters for each model, especially XGBoost.
Feature Engineering: Explore more advanced feature engineering techniques to potentially create more predictive variables.
Advanced Evaluation Metrics: Investigate additional evaluation metrics and techniques, such as ROC curves and AUC, especially if dealing with imbalanced classes.
Deployment: Consider deploying the trained model as a web service or API for real-time predictions.
External Validation: Test the model's performance on independent external datasets to ensure generalization.

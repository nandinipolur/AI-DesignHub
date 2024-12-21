Aircraft Predictive Maintenance using Intel Optimizations
This project implements an Aircraft Predictive Maintenance system using machine learning models optimized for high performance with Intel technologies. The system predicts the Remaining Useful Life (RUL) of aircraft engines and provides insights into potential failures.

Dataset Description
The dataset used for this project consists of three files:

PM_train.txt - Training data with engine operational cycles and sensor measurements.
PM_test.txt - Testing data with engine operational cycles and sensor measurements.
PM_truth.txt - Actual RUL values for engines in the test data.

The dataset includes:
Engine operational settings and sensor readings (setting1, setting2, setting3, s1 to s21).
Engine IDs and operational cycles.
RUL calculated for each engine.
Key Features of the Project

Intel Optimization:
Utilized Intel Extension for Scikit-learn and Intel-optimized XGBoost for faster model training and inference.
Modin library was employed for efficient data processing with Intel-optimized Pandas.

Data Preprocessing:
Calculated the Remaining Useful Life (RUL) for both training and test datasets.
Applied StandardScaler for normalization of sensor features.

Model Training:
Used an Intel-optimized XGBoost regressor to predict RUL.
Parameters: tree_method="hist", predictor="cpu_predictor", n_estimators=100, max_depth=6.

Binary Classification:
Defined a binary classification threshold (w1 = 30 cycles) to classify engine failures.

Evaluated model performance using:
Confusion Matrix
ROC Curve
Accuracy Score

Model Insights:
Visualized feature importance using SHAP (SHapley Additive exPlanations) for interpretability.

Results Visualization:
Plotted Actual vs Predicted RUL for test samples.
Visualized model with confusion matrix.

Model Saving:
Saved the trained XGBoost model in JSON format for easy deployment.

Results
Confusion Matrix: Visualized actual vs. predicted outcomes for binary classification.
ROC Curve: Demonstrated high AUC for the test data.
Test Accuracy: Achieved competitive accuracy in RUL prediction and classification.

Libraries and Tools Used
Intel Technologies:
Intel Extension for Scikit-learn
Intel-optimized XGBoost

Machine Learning:
Scikit-learn, TensorFlow, SHAP

Data Processing:
Modin (Pandas with Intel optimizations)

Visualization:
Matplotlib, Seaborn

Model Deployment:
OpenVINO Toolkit (planned)

# CMAPSS_remaining_life.
# Turbofan Engine Degradation Prediction on NASA C-MAPSS

This project is based on the original repository:
[Predicting-of-Turbofan-Engine-Degradation-Using-the-NASA-C-MAPSS-Dataset](https://github.com/shining0611armor/Predicting-of-Turbofan-Engine-Degradation-Using-the-NASA-C-MAPSS-Dataset)

The original work focused on deep learning approaches such as CNN-LSTM, LSTM, and CNN for Remaining Useful Life (RUL) prediction and health-state classification using the NASA C-MAPSS dataset.

## Additional Implementations Added

Compared to the original GitHub repository, the following extensions were implemented in this project:

### 1. Random Forest Model
A Random Forest model was added as a machine learning baseline for both:
- Regression: RUL prediction
- Classification: engine health state prediction

The same preprocessed dataset and window-based input pipeline were reused so that the comparison with the original deep learning models remains fair.

### 2. XGBoost Model
An XGBoost model was also implemented for both:
- Regression
- Classification

This was added to compare tree-based boosting methods against the original CNN-LSTM, LSTM, and CNN architectures.

### 3. Fair Model Comparison Framework
A structured comparison pipeline was created so that the models can be evaluated under the same dataset flow:
- same cleaned and normalized input data
- same selected sensor features
- same windowing strategy
- same target generation
- same evaluation metrics

### 4. Additional Evaluation Metrics
The project compares models using the following metrics:

#### Regression
- RMSE
- MSE
- MAE
- MAPE

#### Classification
- Accuracy
- Precision
- Recall
- F1-score

### 5. Comparison Tables and Visualizations
Additional summary tables and plots were created to compare the performance of:
- CNN-LSTM
- Random Forest
- XGBoost

These comparison outputs make it easier to identify the best-performing model for regression and classification tasks.

### 6. SHAP-Based Model Interpretability
SHAP (SHapley Additive exPlanations) was added for the tree-based models, especially XGBoost and Random Forest, to improve interpretability.

SHAP was used to:
- identify the most important input features
- understand feature contribution to model predictions
- provide explainability in addition to predictive performance

This addition makes the project stronger by not only comparing accuracy, but also explaining model behavior.

## Project Objective
The goal of this extended project is to predict turbofan engine degradation using NASA C-MAPSS data and to compare deep learning models with traditional machine learning and boosting-based models.

## Models Included
- CNN-LSTM
- LSTM
- CNN
- Random Forest
- XGBoost

## Key Contribution of This Extension
The main contribution of this work over the original repository is the addition of:
- machine learning baseline models
- boosting-based models
- unified comparison framework
- interpretability using SHAP

This allows the project to move beyond only deep learning evaluation and provide a broader, more explainable benchmarking study for turbofan engine degradation prediction.

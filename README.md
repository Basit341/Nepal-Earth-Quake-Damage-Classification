# Nepal Earthquake Damage Prediction

This project predicts the severity of building damage caused by the Nepal earthquake using various machine learning classifiers, including Random Forest, XGBoost, and LightGBM. The workflow includes data preprocessing, feature engineering, model training, hyperparameter tuning, and evaluation.

## Dataset
The dataset is sourced from Kaggle: [Earthquake-Damage-and-Impact](https://www.kaggle.com/datasets/arashnic/earthquake-magnitude-damage-and-impact?select=csv_building_structure.csv)

## Workflow
- **Data Loading & Cleaning:**
  - Loads building structure data and removes duplicates and missing values.
  - Drops leaky, high-cardinality, and multicollinear features.
  - Creates a binary target variable `severe_damage` based on the original damage grade.
- **Feature Engineering:**
  - One-hot encodes categorical features such as land surface condition, foundation type, roof type, etc.
- **Modeling:**
  - Splits data into training and test sets (80/20 split).
  - Trains and evaluates various classification models, including Random Forest, XGBoost, and LightGBM.
  - Performs hyperparameter tuning using RandomizedSearchCV to optimize model performance for each model.
- **Evaluation:**
  - Reports accuracy on both training and test sets for each model.
  - The Random Forest model achieved a test accuracy around 77-78%.

## Requirements
- Python 3.11+
- pandas, numpy, scikit-learn, category_encoders, matplotlib, xgboost, lightgbm

## Usage
1. Place the dataset CSV in the project directory.
2. Run the `random_forest.ipynb` or `xgb_lgbm_boosting_models.ipynb` notebooks to reproduce the analysis and results for different models.

## Results
- The optimized models predict severe building damage with good accuracy.
- The notebooks include code for further evaluation and experimentation.

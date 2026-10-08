# 11 ML Practice Projects

## Folder structure
- `01_titanic_eda_lifecycle.py`
- `02_titanic_preprocessing.py`
- `03_adult_feature_engineering_eda.py`
- `04_california_housing_linear_regularization.py`
- `05_titanic_logistic_regression.py`
- `06_diabetes_multinomial_logistic.py`
- `07_auto_mpg_regression.py`
- `08_heart_decision_tree.py`
- `09_heart_random_forest.py`
- `10_heart_xgb_lightgbm_shap.py`
- `11_wine_quality_tree_random_forest.py`
- `datasets/` -> put downloaded CSV/data files here

## Install
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm shap
```

## Dataset files expected

1. `datasets/titanic_train.csv`
   Kaggle Titanic: https://www.kaggle.com/c/titanic/data

2. `datasets/adult.csv`
   UCI Adult: https://archive.ics.uci.edu/dataset/2/adult

3. California Housing
   No CSV is required. Script downloads it through scikit-learn:
   `fetch_california_housing()`

4. `datasets/diabetes_012_health_indicators_BRFSS2015.csv`
   Kaggle BRFSS Diabetes Health Indicators:
   https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset

5. `datasets/auto-mpg.data`
   UCI Auto MPG:
   https://archive.ics.uci.edu/dataset/9/auto

6. `datasets/heart.csv`
   UCI Heart Disease:
   https://archive.ics.uci.edu/dataset/45/heart+disease
   The script expects the common 14-column form with the final column named `target`.
   If your UCI file uses different names, the script automatically assigns the standard 14 names when `target` is absent.

7. `datasets/winequality-red.csv`
   UCI Wine Quality:
   https://archive.ics.uci.edu/dataset/186/wine+quality
   The white wine file can also be used by changing the filename in script 11.

## Recommended order
1 -> 2 -> 3 -> 4 -> 5 -> 6 -> 7 -> 8 -> 9 -> 10 -> 11

## Important
Project 6 uses a true 3-class diabetes target:
0 = no diabetes, 1 = prediabetes, 2 = diabetes.
This is suitable for multinomial logistic regression. Do not replace it with the Pima dataset without changing the task, because Pima has a binary outcome.

## Dataset notes
- Titanic: survival prediction.
- Adult: income > $50K classification.
- California Housing: median house value regression.
- Auto MPG: fuel-economy regression.
- Heart Disease: binary presence/absence classification derived from the UCI goal field.
- Wine Quality: binary "good wine" classification using quality >= 7.

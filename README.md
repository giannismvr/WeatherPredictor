# Weather Classification Project

## Overview
This project presents an end-to-end binary classification workflow for next-day rain prediction (`RainTomorrow`) using supervised machine learning. The notebook covers data understanding, preprocessing, baseline model comparison, hyperparameter optimization, and export of prediction files.

## Dataset
- Training/validation file: `train-val.csv`
- Test file: `test.csv`
- Target variable: `RainTomorrow`
- Identifier column: `ID` (preserved for final prediction files)

## Methodology
1. **Exploratory analysis** of sample size, feature types, class distribution, and numeric correlations.
2. **Preprocessing pipeline** with `ColumnTransformer`:
   - Numeric: mean imputation + standardization
   - Categorical: most-frequent imputation + one-hot encoding
   - `Date` transformed to month to capture seasonality
3. **Data split** into 70% training and 30% validation sets.
4. **Baseline training** and F1-based comparison across multiple classifiers.
5. **Hyperparameter tuning** using `GridSearchCV` with 5-fold cross-validation.
6. **Final inference** on preprocessed test data and CSV export.

## Models Evaluated
- Gaussian Naive Bayes
- K-Nearest Neighbors
- Logistic Regression
- Multi-Layer Perceptron (MLP)
- Support Vector Classifier (SVC)
- Decision Tree
- Random Forest

## Outputs
The notebook generates prediction files in the required two-column format (`ID`, `Prediction`):
- `predictions_baseline.csv`
- `predictions_tuned.csv`

## Repository Files
- `WeatherPredictor.ipynb`: main notebook implementation
- `train-val.csv`: training/validation dataset
- `test.csv`: held-out test dataset
- `predictions_baseline.csv`: baseline/best-model predictions
- `predictions_tuned.csv`: tuned-model predictions

## Reproducibility
From the project root:

```bash
jupyter notebook WeatherPredictor.ipynb
```

## Notes
This is a structured, reproducible machine learning project suitable for portfolio presentation.

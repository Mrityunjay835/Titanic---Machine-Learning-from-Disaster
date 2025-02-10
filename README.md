# Titanic Survival Prediction

## Project Overview
This project analyzes the Titanic dataset and predicts passenger survival using a Random Forest classifier. The dataset is sourced from Kaggle's Titanic competition.

## Dataset
The dataset contains information about Titanic passengers, including their age, sex, class, and whether they survived the disaster. The data is split into:
- **train.csv**: Contains labeled data used for model training.
- **test.csv**: Contains unlabeled data for making predictions.

## Data Preprocessing
1. **Loading Data**: Data is imported from Kaggle.
2. **Exploratory Data Analysis (EDA)**:
   - Display first few rows of the dataset using `head()`.
   - Compute survival rates for men and women.
3. **Feature Selection**:
   - Selected features: `Pclass`, `Sex`, `SibSp`, `Parch`.
   - Converted categorical `Sex` column to numeric values using `pd.get_dummies()`.

## Model Training
- Utilized **Random Forest Classifier** with:
  - `n_estimators=100`
  - `max_depth=5`
  - `random_state=1`
- Trained the model using the `train.csv` dataset.
- Predicted survival outcomes for the `test.csv` dataset.

## Predictions & Submission
- Predictions were saved in `submission.csv` in the format required by Kaggle.
- Format: `PassengerId, Survived`.
- Output message: *"Your submission was successfully saved!"*

## Dependencies
- Python 3
- NumPy
- Pandas
- Scikit-learn
- Kaggle API (for dataset retrieval)

## How to Run
1. Install necessary libraries:
   ```sh
   pip install numpy pandas scikit-learn kaggle
   ```
2. Authenticate Kaggle:
   ```python
   import kagglehub
   kagglehub.login()
   ```
3. Run the script to train the model and generate predictions.
4. Submit `submission.csv` to Kaggle.

## Results
- **Women survival rate**: ~74.2%
- **Men survival rate**: ~18.9%
- **Random Forest Model Accuracy**: To be evaluated using cross-validation or test data.

## Future Improvements
- Handle missing values in `Age` and `Cabin`.
- Include more features like `Fare`, `Embarked`.
- Try different models like SVM, Logistic Regression.

---
This project provides a basic Titanic survival prediction model. Further tuning and feature engineering can improve accuracy!


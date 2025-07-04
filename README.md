# LoanDefaultPrediction

## Overview

This project tackles the problem of predicting loan defaults using real-world financial data. The goal is to build a machine learning model that can identify borrowers who are most likely to default, enabling financial institutions to better manage risk and make informed lending decisions.

## Dataset

- **train.csv**: Contains records for 255,347 borrowers, including features and a `Default` column indicating whether the borrower defaulted.
- **test.csv**: Contains similar features for 109,435 borrowers, but without the `Default` column. The task is to predict the probability of default for these borrowers.
- **data_descriptions.csv**: Provides descriptions for each feature in the datasets.

## Approach

1. **Data Exploration & Cleaning**
   - Checked for missing and duplicate values (none found).
   - Explored data types, distributions, and feature statistics.
   - Visualized the target variable and feature relationships.

2. **Feature Engineering**
   - Applied one-hot encoding to categorical variables.
   - Scaled features using `StandardScaler` for model stability.

3. **Modeling**
   - Built a baseline logistic regression model.
   - Evaluated model performance using ROC AUC on a validation set.
   - Generated predictions for the test set in the required submission format.

4. **Submission**
   - Created a `prediction_df` with columns `LoanID` and `predicted_probability`.
   - Exported predictions to `prediction_submission.csv` for autograding.

## How to Run

1. Install required packages:
   ```
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```
2. Open and run the notebook `LoanDefaultPrediction.ipynb` step by step.
3. The notebook will output a `prediction_submission.csv` file ready for submission.

## Next Steps & Improvements

- Try advanced models like Random Forest, XGBoost, or LightGBM.
- Perform feature selection and engineering for better predictive power.
- Tune model hyperparameters using cross-validation.
- Address class imbalance if present.

## License

This project is for educational purposes.
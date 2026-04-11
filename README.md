# Employee Promotion Prediction

This project builds a machine learning model to predict whether an employee is likely to be promoted, using an open HR analytics dataset.

## Project Objective
The goal of this project is to develop a simple and interpretable HR analytics pipeline that can support promotion-related decision-making. This project is designed as a learning and portfolio project for machine learning in people analytics and industrial-organisational psychology contexts.

## Dataset
The dataset used in this project is a public HR analytics dataset from Kaggle. It includes employee-related variables such as:

- department
- education
- gender
- recruitment_channel
- no_of_trainings
- age
- previous_year_rating
- length_of_service
- KPIs_met >80%
- awards_won?
- avg_training_score

Target variable:
- `is_promoted`

This project uses the public **HR Analytics** dataset from Kaggle:

[HR Analytics Dataset](https://www.kaggle.com/datasets/arashnic/hr-ana?resource=download)

**Note:** The raw dataset is not included in this repository. It should be downloaded directly from Kaggle.

## Workflow
The project follows these steps:

1. Data loading and inspection
2. Column name cleaning
3. Train-test split
4. Preprocessing with:
   - missing value imputation
   - scaling for numerical features
   - one-hot encoding for categorical features
5. Model training
6. Model comparison
7. Feature importance analysis
8. Threshold tuning
9. Final model saving

## Models Used
Two classification models were compared:

- Logistic Regression
- Random Forest

## Results
The best baseline model was **Random Forest**.

### Baseline Random Forest Performance
- Accuracy: 0.9219
- Precision: 0.5598
- Recall: 0.3908
- F1-score: 0.4603
- ROC-AUC: 0.8016

### After Threshold Tuning
- Precision: 0.5287
- Recall: 0.4143
- F1-score: 0.4646

Threshold tuning slightly improved the F1-score and recall, while precision decreased slightly.

## Key Findings
The most important predictors of promotion were:

- avg_training_score
- department
- previous_year_rating
- awards_won

The feature `no_of_trainings` had negligible predictive importance in the final model.

## Files
- `employee_promotion_prediction.ipynb` → main notebook
- `best_employee_promotion_model.pkl` → saved trained model
- `requirements.txt` → required libraries

## Tools and Libraries
- Python
- Google Colab
- pandas
- numpy
- matplotlib
- scikit-learn
- joblib

## Notes
This project is intended as a portfolio project for learning machine learning in HR analytics, people analytics, and organisational research contexts. It should be interpreted as decision support rather than automated decision-making.

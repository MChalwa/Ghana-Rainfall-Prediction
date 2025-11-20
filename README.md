# Ghana-Rainfall-Prediction
This project builds an end-to-end machine learning pipeline to predict rainfall intensity (No Rain, Small Rain, Medium Rain, Heavy Rain) using meteorological indicators.
## Project Overview
This project develops an end-to-end machine learning pipeline to classify rainfall intensity into four categories:

- NORAIN

- SMALLRAIN

- MEDIUMRAIN

- HEAVYRAIN

Using historical meteorological data, the model learns patterns from indicators such as dew, fog, wind, clouds, heat, lightning, and more.
The project is part of a broader initiative to improve early rainfall forecasting and support climate-related decision-making.

## Key Features
1. Cleaned and preprocessed meteorological data

2. Filled missing indicator values based on domain-driven mapping

3. Built a unified preprocessing and modeling pipeline using ColumnTransformer + Pipeline

4. Compared multiple machine learning algorithms:

    - Logistic Regression

    - Decision Tree

    - Random Forest

    - SVM

    - XGBoost

    - LightGBM

    - CatBoost

CatBoost achieved the best performance (F1-score: 0.95)

5. Generated predictions for the test dataset

6. Prepared final id and Target submission file

## Modeling Approach
1. Data Preprocessing

Handled missing values

Encoded the target variable

Applied One-Hot Encoding to categorical features

Scaled numeric features

2. Model Training & Evaluation

Evaluated multiple models on the validation set using F1-score.
CatBoost performed best due to its ability to handle categorical data efficiently.

3. Final Prediction

The best model was retrained on the full training data

Predictions were generated for the unseen test dataset

Output saved as a submission file
## Conclusions

1. Machine learning techniques can effectively predict rainfall intensity in Ghana, with several models achieving high accuracy and strong F1-scores (>95%) on the validation set.

    - CatBoost, XGBoost, and LightGBM performed the best, indicating that gradient boosting algorithms handle mixed feature types and nonlinear weather patterns exceptionally well.

2. The feature engineering steps, especially imputing weather indicators using domain logic, improved model robustness and helped the classifiers better recognize rainfall patterns.

3. Despite being a multi-class problem with imbalanced target labels, the models were able to accurately classify all four rainfall categories (No Rain, Small Rain, Medium Rain, Heavy Rain).

4. The final selected model (e.g., CatBoost) generated consistent predictions on the test dataset, enabling a reliable submission file containing the ID and predicted Target labels.

5. The project highlights how data science and climate analytics can support early warning systems and improve short-term rainfall forecasting — especially valuable for agriculture, disaster preparedness, and local weather decision-making.

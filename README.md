# modelswithtitanicdf
 Predicting survival on the Titanic (common dataset) using: logistic model-random forest-stacking-XGBoost

# Titanic Survival Analysis: A Predictive Modeling Exercise

This repository presents an analysis of passenger survival on the Titanic using machine learning techniques.  The Titanic dataset, while frequently used as a teaching example, provides a valuable opportunity to apply and compare different predictive modeling methods. This project focuses on predicting the probability of passenger survival before embarking, utilizing readily available passenger data.


## Methodology

This analysis was conducted using the R programming language and several data analysis and machine learning libraries. The process involved these key steps:

**1. Data Cleaning and Preprocessing:** The dataset was cleaned and prepared for modeling. This included handling missing values using `na.omit()`, converting categorical variables to factors using `factor()`, and appropriate transformations of numerical variables.  Column names were standardized for consistency.  This preprocessing step is crucial for ensuring the reliability and accuracy of the subsequent analysis.

**2. Data Splitting:** The dataset was divided into training (80%) and testing (20%) sets using a random seed (`set.seed(123)`) for reproducibility. This split is vital for evaluating the models' ability to generalize to unseen data.

**3. Predictive Modeling:** Several machine learning models were trained to predict survival:

* **Logistic Regression:** This model was used to establish a relationship between passenger characteristics and survival.  Coefficient analysis provided insight into the impact of each feature on survival probability.

* **Random Forest:** A Random Forest model was employed to capture potential complex interactions between variables and improve predictive accuracy.  Variable importance was assessed to identify the most significant predictors.

* **XGBoost:**  This gradient boosting algorithm was used to further enhance predictive performance by leveraging an ensemble approach.  Hyperparameter tuning was implemented to optimize the model's efficiency and accuracy.

**4. Model Evaluation:**  Model performance was evaluated using metrics such as the Area Under the Curve (AUC) of the Receiver Operating Characteristic (ROC) curve, and the confusion matrix.  The AUC provides a measure of a model's ability to distinguish between survivors and non-survivors.  The confusion matrix gives a detailed breakdown of correct and incorrect classifications.

## Results

The models achieved varying levels of accuracy in predicting passenger survival.  The XGBoost model demonstrated the highest performance, achieving an AUC of approximately 0.9133. This suggests that the model is quite accurate at distinguishing between survivors and non-survivors. The confusion matrices provide additional detail on the specific types of prediction errors made by each model.

## Conclusions

This project showcases the application of various machine learning techniques to a classic predictive modeling problem. While using a well-known dataset, the project effectively demonstrates data preprocessing, model selection, and evaluation procedures.  The results suggest that XGBoost is a particularly effective model for this task.  The dataset utilized in this project is publicly available and included in the 'Data' folder.

## Technologies Used

* R
* RStudio
* Git
* GitHub
* `readr`, `dplyr`, `ggplot2`, `randomForest`, `caret`, `pROC`, `xgboost`

## How to Run the Code

1. Clone this repository.
2. Install the necessary R packages listed above.
3. Run the `Análisis_Titanic.Rmd` file using RStudio. The `Data/titanic.csv` file contains the dataset.

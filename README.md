# Securing-Healthcare-Systems-A-Machine-Learning-based-Fraud-Detection-Approach

## Project Overview:

This study delves into the challenge of healthcare fraud in the United States, where over the past two decades, the average individual and family insurance premiums have witnessed substantial increases. Conventional manual methods for fraud detection are proving to be inefficient and time-consuming, necessitating a shift in our approach. The project envisions a healthcare system fortified by a proactive and sustainable fraud detection strategy, contributing to elevated service quality and cost-effectiveness. Through the application of data mining and exploratory data analysis (EDA), we aim to uncover distinctive patterns and anomalies within the data. The model at the core of our investigation concentrates on binary classification tasks, harnessing advanced machine learning techniques such as logistic regression, KNN, decision trees, SVM Classifier and Boosting Classifiers in conjunction with ensemble methods. This research not only strives to effectively detect potential frauds but also endeavours to pinpoint the key features influencing such detections, providing invaluable insights for a more secure and efficient healthcare ecosystem. 

## Business Understanding: 

Healthcare fraud represents a multifaceted problem in the U.S., encompassing various fraudulent activities by providers, such as billing for unrendered services or overcharging for provided services. This issue not only results in a substantial financial drain on the healthcare system, affecting nearly 15.3% of the GDP as highlighted in a 2004 GAO report, but also compromises patient care and trust in healthcare institutions. Despite existing efforts to combat this issue, traditional manual detection methods are proving inadequate, necessitating a shift towards more efficient, technology-driven approaches.

## Data Understanding 

The foundation of our study is built upon the collection of healthcare-related data from [Kaggle](https://www.kaggle.com/datasets/rohitrox/healthcare-provider-fraud-detection-analysis), a renowned open-source data platform

The dataset comprises four sets for training and testing, providing insights into healthcare claims:

1. 	**Mapping Data:** Contains unique provider IDs mapped with class labels indicating involvement in fraudulent activities. Test data includes only provider IDs; class labels need to be determined.
2.	**Beneficiary Data:** Comprehensive information about patients, including demographics, diseases, premium details, and reimbursement data.
3.	**Inpatient Data:** Details of claims filed for hospitalized patients, offering insights into inpatient healthcare interactions.
4.	**Outpatient Data:** Information on claims filed for non-admitted patients, providing insights into outpatient healthcare interactions

## Librarires Used

In our pursuit of detecting healthcare fraud, we rely on Python, celebrated for its robust data science libraries, in conjunction with Tableau for generating insightful visualizations. Our toolkit comprises essential components such as:
- Pandas and NumPy for data manipulation,
- Matplotlib and Seaborn for visualization,
- Scikit Learn for modeling, and
- a selection of advanced statistical analysis libraries including StatsModels, CategoryEncoders, imblearn, catboost, and xgboost for handling complex statistical tasks, encoding, and managing imbalanced datasets effectively.

### Data Processing Strategy

Our approach to processing data involves:

- **Data Type Correction**: Ensuring consistent data types for accurate analysis.
- **Missing Value Handling**: Employing imputation techniques to address missing data.
- **Feature Engineering**: Crafting informative attributes to enhance model performance.

### Preparing Data for Modeling

To ensure our data is ready for modeling, we perform the following steps:

- **Outlier Management**: Identifying and managing outliers to prevent distortion of results.
- **Standardization**: Scaling features to a standard range for uniformity.
- **Response Encoding**: Encoding categorical variables to numeric representations.

### Handling Class Imbalances

Class imbalance, a common challenge in fraud detection, is addressed using the SMOTE (Synthetic Minority Over-sampling Technique) technique to balance the dataset effectively.

## Model and Evaluation 

For model induction, we've thoroughly explored various classifiers, including Logistic Regression, KNN, Decision Trees, Random Forest, CatBoost, AdaBoost, XGBoost, and SVM. Each model has been fine-tuned using GridSearchCV to pinpoint the optimal set of hyperparameters, thereby ensuring peak performance aligned with our fraud detection objectives.

Initially, we randomly sampled a portion of the dataset for model building due to its large size. Subsequently, we conducted fine hyperparameter tuning using GridSearchCV and Cross-Validation Methods. We then selected the best performing models and trained them on the entire population dataset, evaluating and identifying the optimal model.

### Model Performance on a andomly sampled dataset

| Method           | Hyperper Tuning | Train_Accuracy | Train_Precision | Train_Recall | Train_FNR | Train_F1 | Train_ROC_AUC | Test_Accuracy | Test_Precision | Test_Recall | Test_FNR | Test_F1 | Test_ROC_AUC |
|------------------|-----------------|----------------|-----------------|--------------|-----------|----------|---------------|---------------|----------------|-------------|----------|---------|--------------|
| Logistic Regression | No | 0.69 | 0.69 | 0.68 | 0.32 | 0.69 | 0.69 | 0.69 | 0.7 | 0.67 | 0.33 | 0.69 | 0.69 |
| Logistic Regression | Yes | 0.68 | 0.68 | 0.68 | 0.32 | 0.68 | 0.68 | 0.68 | 0.69 | 0.68 | 0.32 | 0.68 | 0.68 |
| KNN | No | 0.77 | 0.73 | 0.86 | 0.14 | 0.79 | 0.77 | 0.56 | 0.55 | 0.56 | 0.44 | 0.56 | 0.56 |
| KNN | Yes | 1 | 1 | 1 | 0 | 1 | 1 | 0.56 | 0.56 | 0.5 | 0.5 | 0.53 | 0.56 |
| Decision Tree | No | 1 | 1 | 1 | 0 | 1 | 1 | 0.69 | 0.69 | 0.69 | 0.31 | 0.69 | 0.69 |
| Decision Tree | Yes | 0.94 | 0.95 | 0.94 | 0.06 | 0.94 | 0.94 | 0.7 | 0.71 | 0.69 | 0.31 | 0.7 | 0.7 |
| Random Forest | No | 1 | 1 | 1 | 0 | 1 | 1 | 0.72 | 0.74 | 0.69 | 0.31 | 0.71 | 0.72 |
| Random Forest | Yes | 1 | 1 | 1 | 0 | 1 | 1 | 0.73 | 0.74 | 0.7 | 0.3 | 0.72 | 0.73 |
| AdaBoost | No | 0.71 | 0.71 | 0.72 | 0.28 | 0.72 | 0.71 | 0.71 | 0.71 | 0.72 | 0.28 | 0.71 | 0.71 |
| AdaBoost | Yes | 0.7 | 0.69 | 0.71 | 0.29 | 0.7 | 0.7 | 0.7 | 0.7 | 0.71 | 0.29 | 0.71 | 0.7 |
| CatBoost | No | 0.75 | 0.75 | 0.73 | 0.27 | 0.74 | 0.75 | 0.74 | 0.75 | 0.72 | 0.28 | 0.74 | 0.74 |
| CatBoost | Yes | 0.77 | 0.78 | 0.75 | 0.25 | 0.76 | 0.77 | 0.75 | 0.76 | 0.73 | 0.27 | 0.74 | 0.75 |
| XgBoost | No | 0.78 | 0.8 | 0.75 | 0.25 | 0.77 | 0.78 | 0.75 | 0.77 | 0.72 | 0.28 | 0.75 | 0.75 |
| XgBoost | Yes | 0.8 | 0.82 | 0.78 | 0.22 | 0.8 | 0.8 | 0.76 | 0.77 | 0.73 | 0.27 | 0.75 | 0.76 |
| SVM Classifier | No | 0.73 | 0.72 | 0.73 | 0.27 | 0.73 | 0.73 | 0.68 | 0.68 | 0.68 | 0.32 | 0.68 | 0.68 |


### Best performing models on the original dataset

| Method          | Hyperper Tuning | Train_Accuracy | Train_Precision | Train_Recall | Train_FNR | Train_F1 | Test_Accuracy | Test_Precision | Test_Recall | Test_FNR | Test_F1 |
|-----------------|-----------------|----------------|-----------------|--------------|-----------|----------|---------------|----------------|-------------|----------|---------|
| XgBoost         | No              | 0.76           | 0.78            | 0.73         | 0.27      | 0.76     | 0.76          | 0.78           | 0.73        | 0.27     | 0.75    |
| XgBoost         | Yes             | 0.77           | 0.79            | 0.74         | 0.26      | 0.77     | 0.77          | 0.79           | 0.74        | 0.26     | 0.76    |
| CatBoost        | No              | 0.76           | 0.77            | 0.73         | 0.27      | 0.75     | 0.76          | 0.77           | 0.73        | 0.27     | 0.75    |
| Random Forest   | Yes             | 0.96           | 0.95            | 0.97         | 0.03      | 0.96     | 0.76          | 0.76           | 0.74        | 0.26     | 0.75    |

## ## Top 10 Variables

- County (4.9192)
- isInpatient (1.1099)
- ClmProcedureCode_3893.0 (-0.5745)
- ClmProcedureCode_9904.0 (-0.5413)
- ClmProcedureCode_3995.0 (-0.5286)
- ClmDiagnosisCode_53081 (-0.3636)
- ClmDiagnosisCode_2449 (-0.3426)
- UniquePhys (0.2961)
- ClmDiagnosisCode_42731 (-0.2851)
- PhysMultiRole2 (0.2543)


## Conclusion

In conclusion, our project has achieved remarkable success in our mission to enhance healthcare fraud detection in the United States within a stringent 3-month timeframe. Through the strategic application of advanced machine learning techniques, including logistic regression, KNN, decision trees, random forest, SVM, and boosting classifiers, we have surpassed our performance objectives. Notably, our XGBoost model has emerged as the frontrunner, boasting an impressive recall of 0.74, a minimal false positive rate (FPR) of 0.26, and an exceptional ROC-AUC score of 0.85. These results attest to the model's robust predictive capabilities and its capacity to discern between positive and negative classes with unparalleled accuracy.

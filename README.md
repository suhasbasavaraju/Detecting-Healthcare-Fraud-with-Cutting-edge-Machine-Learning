# Securing-Healthcare-Systems-A-Machine-Learning-based-Fraud-Detection-Approach

## Project Overview:

This study delves into the challenge of healthcare fraud in the United States, where over the past two decades, the average individual and family insurance premiums have witnessed substantial increases. Conventional manual methods for fraud detection are proving to be inefficient and time-consuming, necessitating a shift in our approach. The project envisions a healthcare system fortified by a proactive and sustainable fraud detection strategy, contributing to elevated service quality and cost-effectiveness. Through the application of data mining and exploratory data analysis (EDA), we aim to uncover distinctive patterns and anomalies within the data. The model at the core of our investigation concentrates on binary classification tasks, harnessing advanced machine learning techniques such as logistic regression, KNN, decision trees, SVM Classifier and Boosting Classifiers in conjunction with ensemble methods. This research not only strives to effectively detect potential frauds but also endeavours to pinpoint the key features influencing such detections, providing invaluable insights for a more secure and efficient healthcare ecosystem. 

## Business Understanding: 

Healthcare fraud represents a multifaceted problem in the U.S., encompassing various fraudulent activities by providers, such as billing for unrendered services or overcharging for provided services. This issue not only results in a substantial financial drain on the healthcare system, affecting nearly 15.3% of the GDP as highlighted in a 2004 GAO report, but also compromises patient care and trust in healthcare institutions. Despite existing efforts to combat this issue, traditional manual detection methods are proving inadequate, necessitating a shift towards more efficient, technology-driven approaches.

## Data Understanding 

The foundation of our study is built upon the collection of healthcare-related data from [Kaggle](https://www.kaggle.com/datasets/rohitrox/healthcare-provider-fraud-detection-analysis), a renowned open-source data platform

The dataset comprises four sets for training and testing, providing insights into healthcare claims:

1. 	Mapping Data: Contains unique provider IDs mapped with class labels indicating involvement in fraudulent activities. Test data includes only provider IDs; class labels need to be determined.
2.	Beneficiary Data: Comprehensive information about patients, including demographics, diseases, premium details, and reimbursement data.
3.	Inpatient Data: Details of claims filed for hospitalized patients, offering insights into inpatient healthcare interactions.
4.	Outpatient Data: Information on claims filed for non-admitted patients, providing insights into outpatient healthcare interactions

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





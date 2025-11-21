# Google Advanced Data Analytics Capstone 
## Salifort Employee Retention Project

## Table of Contents
- [Data Source](#data-source)
- [Libraries used](#libraries-used)
- [EDA and Data Preparation}](#eda-and-data-analysing) 
- [Data Preparation for Modeling](#data-preparation-for-modeling)
- [Modeling: XGBoost Binomial Classification](#modeling-xgboost-binomial-classification)
  - [Model Results on Training Data](#model-results-on-training-data)
  - [XGBoost Predict on Validation Data](#xgboost-predict-on-validation-data)
  - [XGBoost Predict on Test Data](#xgboost-predict-on-test-data)
- [Conclusion and Insights](#conclusion-and-insights)
- [Recommendation and Next Steps](#recommendation-and-next-steps)

### Data Source
- Salifort Employee Data from [Kaggle.](https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction?select=HR_comma_sep.csv)
![data_description](https://github.com/myroslavnatalchenko/Google_Advanced_Data_Analytics_Capstone/img/data_secription.png)

### Libraries used
- Pandas: Used for data manipulation, cleaning, and tabular analysis
- NumPy: Employed for high-performance numerical computing and array operations
- Matplotlib / Seaborn: Utilized for Exploratory Data Analysis (EDA) and creating static visualizations
- Scikit-learn: The core library used for building and evaluating machine learning models, specifically Decision Tree and Random Forest Classifiers, as well as for preprocessing and cross-validation
- XGBoost: Applied for advanced gradient boosting (XGBClassifier) to achieve higher predictive accuracy and analyze feature importance

### EDA and Data Preparation
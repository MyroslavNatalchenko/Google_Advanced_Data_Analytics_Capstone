# Google Advanced Data Analytics Capstone 
## Salifort Employee Retention Project

## Table of Contents
- [Data Source](#data-source)
- [Libraries used](#libraries-used)
- [EDA and Data Preparation}](#eda-and-data-preparation) 
- [Summary of model results](#summary-of-model-results)
- [Feature Importance](#feature-importance)
- [Conclusion and Insights](#conclusion-and-insights)

### Data Source
- Salifort Employee Data from [Kaggle.](https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction?select=HR_comma_sep.csv)
![data_description](https://github.com/MyroslavNatalchenko/Google_Advanced_Data_Analytics_Capstone/blob/main/img/data_description.png)

### Libraries used
- Pandas: Used for data manipulation, cleaning, and tabular analysis
- NumPy: Employed for high-performance numerical computing and array operations
- Matplotlib & Seaborn: Utilized for Exploratory Data Analysis (EDA) and creating static visualizations
- Scikit-learn: The core library used for building and evaluating machine learning models, specifically Decision Tree and Random Forest Classifiers, as well as for preprocessing and cross-validation
- XGBoost: Applied for advanced gradient boosting (XGBClassifier) to achieve higher predictive accuracy and analyze feature importance

### EDA and Data Preparation
Analyzed the class distribution of the target variable. The dataset reveals a 16.6% attrition rate, while 83.4% of employees remained. This proportion is consistent across all departments, indicating no specific department has a significantly higher turnover rate.

- Categorical data -> numeric data
  - Changed Salary: [low, medium, high] -> [0, 1, 2]
  - Converted Department column into numeric values with help of pd.get_dummies

### Summary of model results
| model | precision | recall | F1 | accuracy | auc |
|  :--- | :--- | :--- | :--- | :--- | :--- |
| Decision Tree CV | 0.92324 | 0.91561 | 0.91934 | 0.97331 | 0.97049 |
| XGBoost CV | 0.96487 | 0.91829 | 0.94098 | 0.98087 | 0.98693 |
| Random Forest CV | 0.95067 | 0.91561 | 0.93279 | 0.97809 | 0.98133 |
| XGBoost Test | 0.96855 | 0.92771 | 0.94769 | 0.98299 | 0.96086 |
| Decision Tree FE CV | 0.95858 | 0.91427 | 0.9359 | 0.97921 | 0.97039 |
| XGBoost FE CV | 0.96887 | 0.91695 | 0.94218 | 0.98132 | 0.98496 |
| Random Forest FE CV | 0.94166 | 0.90824 | 0.92464 | 0.97543 | 0.98062 |
| XGBoost FE Test | 0.95833 | 0.92369 | 0.9407 | 0.98065 | 0.95785 |
**Logistic Regression**

The logistic regression model achieved (all weighted averages):
- precision: 79%
- recall: 82%
- accuracy of 83%
- F1-score: 80%

**Tree-based Machine Learning**

After feature engineering:
- Decision Tree on Validation Set:
    - precision: 95.85%
    - recall: 91.47%
    - accuracy: 97.92%
    - F1-score: 93.59%
    - AUC: 97.03%
- Random Forest on Validation Set:
    - precision: 94.16%
    - recall: 90.82%
    - accuracy: 97.54%
    - F1-score: 92.44%
    - AUC: 98.06%
- XGBoost on Validation Set:
    - precision: 96.88%
    - recall: 91.69%
    - accuracy: 98.13%
    - F1-score: 94.21%
    - AUC: 98.49%
- XGBoost on Test Set:
    - precision: 95.83%
    - recall: 92.36%
    - accuracy: 98.06%
    - F1-score: 94.07%
    - AUC: 95.78%

![feature_importance](https://github.com/MyroslavNatalchenko/Google_Advanced_Data_Analytics_Capstone/blob/main/img/cm.png)

XGBoost outperformed Decision Tree and Random Forest models

### Feature Importance
![feature_importance](https://github.com/MyroslavNatalchenko/Google_Advanced_Data_Analytics_Capstone/blob/main/img/feature_importance.png)

### Conclusion and Insights
The analysis confirms that employee overworking is the primary driver of churn. To improve retention, we recommend:
- Limit Workload: Cap the maximum number of active projects per employee.
- Address Stagnation: Review promotion paths for employees with 4+ years of tenure to address specific dissatisfaction.
- Regulate Overtime: Either explicitly compensate for overtime or strictly enforce standard hours. Ensure policies are transparent.
- Revise Evaluations: Detach high performance scores from excessive working hours (240+/month); reward efficiency over duration.
- Improve Culture: Initiate open discussions to address work culture and expectations at both team and company levels.

## Visulizations used for analysis 
### Number of project counts
![nmb_of_prj_cnt](https://github.com/MyroslavNatalchenko/Google_Advanced_Data_Analytics_Capstone/blob/main/img/nmb_of_prj_cnt.png)
### Monthly hours by number of projects
![mnt_h_prj](https://github.com/MyroslavNatalchenko/Google_Advanced_Data_Analytics_Capstone/blob/main/img/mnt_h_prj.png)
### Employee satisfaction analysis
![emp_anl](https://github.com/MyroslavNatalchenko/Google_Advanced_Data_Analytics_Capstone/blob/main/img/emp_anl.png)
### Employee tenure analysis
![emp_ten](https://github.com/MyroslavNatalchenko/Google_Advanced_Data_Analytics_Capstone/blob/main/img/emp_ten.png)
### Satisfaction vs. Evaluation scatterplot
![st_ev](https://github.com/MyroslavNatalchenko/Google_Advanced_Data_Analytics_Capstone/blob/main/img/st_ev.png)
### Heatmap
![heatmap](https://github.com/MyroslavNatalchenko/Google_Advanced_Data_Analytics_Capstone/blob/main/img/heatmap.png)

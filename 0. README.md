# PROJECT SUMMARY

## NAME
Customer Churn Prediction - Machine Learning Project

## CONTEXT
In the competitive telecom industry, retaining customers is crucial for maintaining revenue and growth. Customer churn, where customers discontinue their service, poses a significant challenge. By predicting churn, companies can take proactive measures to retain customers and improve overall satisfaction.

## GOAL
Develop a machine learning model to predict whether a customer will churn, enabling the company to implement targeted retention strategies.

## DATA
1 CSV file (7043, 21): Customer-Churn.csv

## TECHNIQUES AND LIBRARIES USED:
- Data Acquisition: CSV import with **Pandas**
- Data Analytics: Exploratory data analysis to understand patterns and relationships
- Data Visualization: **Seaborn, Matplotlib and Plotply**
- Data Preprocessing: Cleaning, encoding, and scaling with **Scikit Learn**, **Numpy** and **Scipy**
- Data Engineering: Feature creation, selection, and imputation
- Modeling: Logistic Regression, SVC, Random Forest, and ensemble methods (voting, stacking, boosting) with **Imbalanced-Learn** and Scikit Learn.
- Evaluation: Recall, precision, F1-score, cross-validation, confusion matrix, and learning curve
- Tuning: GridSearchCV/RandomizedSearchCV for parameter optimization
- Deployment: Model saving with **joblib**

## METHODOLOGY

#### Data Acquisition and Preparation:
- Import Data: Loaded dataset using Pandas.
- Data Cleaning: Handled missing values, corrected data types, and dropped unnecessary columns.

#### Exploratory Data Analysis (EDA):
- Descriptive Statistics: Calculated summary statistics.
- Visualization: Used seaborn and matplotlib for histograms, bar plots, and correlation heatmaps.
- Target Variable Analysis: Examined churn distribution and identified class imbalance.

#### Data Preprocessing:
- Encoding Categorical Variables: One-hot and target encoding.
- Scaling: Standardization/normalization of continuous variables.

#### Modeling:

- Model Selection: Choose several classification models suitable for the task (Handling Imbalance).
- Initial Training: Baseline performance with default parameters.
- Evaluation Metrics: Prioritized recall, also considered precision, F1-score, and accuracy.
- Parameter Tuning: Grid search and random search.
- Cross-Validation: Ensured model generalizability and prevented overfitting.

#### Feature Engineering
- Feature Selection: Evaluated feature importance.
- Feature Creation/Deletion: Simplified the model with new and selected features.

#### Model Deployment:
- Final Model Selection: Based on recall and overall performance and tradeoff.
- Saving the Model: Using joblib.
- Wrapper Class: Facilitated easy deployment and integration.

#### Model & Business Recommendations:
- Insights and Strategies: Derived actionable insights and proposed strategies to mitigate churn and improve model accuracy.
- Implementation Plan: A plan for targeted interventions was suggested.


## DATA ANALYSIS

### Observations
- **Churning Rate**: 26.5%
- **Imbalance in Target Class**: 26.5% churn vs 73.5% non-churn.
- **Variable Types**: 17 categoricals, 3 numericals. 
- **Influential Factors**:
  - **Demographics**: 'SeniorCitizen', 'Partner', 'Dependents'
  - **Services**: 'MultipleLines', 'InternetService', 'OnlineSecurity', 'OnlineBackup', 'DeviceProtection', 'TechSupport'
  - **Account**: 'Contract', 'PaperlessBilling', 'PaymentMethod', 'MonthlyCharges', 'TotalCharges', 'tenure'

### Variable Relationships with Churn:
**Categorical variables:**
- Demographic Details:
  - 'SeniorCitizen', 'Partner', 'Dependents': Influence churn rates (e.g., seniors, singles, and independents have higher churn rates).
- Services:
  - 'InternetService': High influence for Fiber optic with a churn rate of 69.4%.
  - Optional Internet Services: decrease churn among internet customers.
- Account Details:
  - 'Contract': Month-to-month contracts see the highest churn rate (88.6%).
  - 'PaperlessBilling': Increases churn (74.9%).
  - 'PaymentMethod': Electronic check payments have the highest churn rate (57.3%).

**Continuous Variables:**
- 'Total Charges': Lower charges, higher churn (new customers).
- 'Tenure': Shorter tenure, higher churn. 75% of churn occurs before 30 months(new customers). 
- 'Monthly Charges': Higher charges, higher churn. Notable increase in churn probability around $65/month.

### Correlation Analysis:
- Internet Services: Strong correlation with optional internet services (+0.61).
- Phone Services: Strong correlation with MultipleLines and PhoneService (+0.61).


## CONCLUSION

### Possible Solutions to Improve Model Performance

- **More Quality Data:** Collect additional customer interaction data.
- **Feature Engineering:** Create new features.
- **Data Augmentation:** Generate synthetic data using SMOTE.
- **Ensemble Methods:** Combine predictions from multiple models.
- **Dimensionality Reduction:** Apply Principal Component Analysis (PCA).
- **Regularization:** Use L1/L2 regularization.
- **Temporal Analysis:** Incorporate time-based features.

### Possible Business Solutions to Improve Customer Churn

#### Proactive Customer Management
- Procedures and warning for high-risk clients
- Early intervention programs

#### Incentives and Rewards
- New customer incentives
- High-paying customer incentives
- Quick surveys with incentives
- Loyalty programs
  
#### Customer Engagement and Support
- Engage unhappy customers
- Enhanced customer support
- Personalized communication
- Customer feedback loop

#### Service and Product Improvement
- Service Quality Improvement
- Customer Education

#### Data-Driven Strategies
- Predictive Analytics

#### Flexibility and Customization
- Flexible Contract Options
- Tailored Offers and Promotions

# Understanding Customer Conversion in Bank Marketing Campaigns

## About the Project
This project analyzes customer subscription behavior in banking marketing campaigns, focusing on term deposits. Direct marketing campaigns often have low conversion rates, leading to inefficiencies and high costs. Using machine learning, this project predicts which customers are more likely to subscribe and identifies the key factors influencing their decisions. The study uses the [UCI Bank Marketing dataset](https://archive.ics.uci.edu/dataset/222/bank+marketing) containing demographic, financial, and campaign-related data for over 41,000 customers.

---

## Tech Stack & Packages
- **Programming Language:** Python 3.x  
- **Data Analysis & Manipulation:** `pandas`, `numpy`  
- **Data Visualization:** `matplotlib`, `seaborn`  
- **Preprocessing & Feature Engineering:** `scikit-learn` (`StandardScaler`, `OneHotEncoder`, `train_test_split`)  
- **Machine Learning Models:** `scikit-learn` (`LogisticRegression`, `RandomForestClassifier`)  
- **Hyperparameter Tuning:** `scikit-learn` (`GridSearchCV`)  
- **Model Evaluation:** `scikit-learn` (`accuracy_score`, `classification_report`, `confusion_matrix`)  
- **Multicollinearity Check:** `statsmodels` (`variance_inflation_factor`)
  
---

## What Was Done
1. **Data Preparation & Cleaning**
   - Removed `duration` to prevent data leakage; converted target variable `y` to binary.  
   - One-hot encoded categorical features and standardized numerical features.  
   - Created `was_contacted_before` from `pdays` and scaled numeric columns.  

2. **Exploratory Data Analysis (EDA)**
   - Visualized class imbalance, feature correlations, and target relationships.  
   - Identified key variables affecting subscription.  

3. **Multicollinearity Handling**
   - Calculated VIF scores; removed highly correlated macroeconomic features for model stability.  

4. **Modeling**
   - Built **Logistic Regression** and **Random Forest** classifiers.  
   - Used GridSearchCV for hyperparameter tuning and `class_weight='balanced'` to handle class imbalance.  
   - Evaluated models using Accuracy, Precision, Recall, F1-score, and Confusion Matrices.  

---

## Results
| Metric | Logistic Regression | Random Forest |
|--------|------------------|---------------|
| Overall Accuracy | 82.48% | 89.18% |
| Precision (Subscribed) | 0.26 | 0.54 |
| Recall (Subscribed) | 0.31 | 0.26 |
| F1-score (Subscribed) | 0.29 | 0.35 |
| False Positives | 803 | 203 |
| False Negatives | 640 | 688 |

---

## Impact
- Helps banks target high-probability subscribers, improving marketing efficiency.  
- Reduces wasted resources and operational costs.  
- Provides actionable insights on customer behavior for future campaigns.  
- Methodology can be applied to other domains like insurance, retail, or subscription services.
 
---

**Insights:**  
- Random Forest outperforms Logistic Regression in overall accuracy and precision for the minority class (subscribers).  
- Both models struggle with recall due to dataset imbalance.  
- Important predictors include age, previous campaign history, and macroeconomic indicators.  
- Class imbalance remains a key challenge; further improvements may require advanced resampling techniques or ensemble methods.

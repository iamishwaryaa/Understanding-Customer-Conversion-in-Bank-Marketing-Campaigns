# Understanding Customer Conversion in Bank Marketing Campaigns

## About the Project
This project analyzes customer subscription behavior in banking marketing campaigns, focusing on term deposits. Direct marketing campaigns often have low conversion rates, leading to inefficiencies and high costs. Using machine learning, this project predicts which customers are more likely to subscribe and identifies the key factors influencing their decisions. The study uses the [UCI Bank Marketing dataset](https://archive.ics.uci.edu/dataset/222/bank+marketing) containing demographic, financial, and campaign-related data for over 41,000 customers.

---

## Tech Stack
- **Programming Language:** Python  
- **Data Analysis & Manipulation:** pandas, NumPy  
- **Data Visualization:** Matplotlib, Seaborn  
- **Preprocessing & Feature Engineering:** One-hot encoding, scaling, handling missing values, feature selection  
- **Machine Learning Models:** Logistic Regression, Random Forest Classifier  
- **Hyperparameter Tuning:** GridSearchCV  
- **Model Evaluation:** Accuracy, Precision, Recall, F1-score, Confusion Matrix, ROC-AUC  
- **Multicollinearity Check:** Variance Inflation Factor (VIF)  

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

**Key Insights:**
- Random Forest achieved higher overall accuracy and better precision for predicting actual subscribers.  
- Class imbalance remains a challenge; models have low recall for subscribers.  
- Campaign-related variables and financial indicators are strong predictors of subscription.  

---

## Impact
- Helps banks target high-probability subscribers, improving marketing efficiency.  
- Reduces wasted resources and operational costs.  
- Provides actionable insights on customer behavior for future campaigns.  
- Methodology can be applied to other domains like insurance, retail, or subscription services.

## Module 20 Report

## Credit-risk-classification

### Overview of the Analysis
The purpose of this analysis was to evaluate the performance of a logistic regression machine learning model for predicting the risk associated with loans using historical lending activity. The dataset used for this analysis included financial information such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, total debt, and loan status. The primary objective is to predict whether a loan would be classified as healthy (low-risk) or high-risk.

The target variable for this prediction is the loan status, which had two possible values: 0 (healthy loan) and 1 (high-risk loan). The initial analysis of the dataset using the 'value_counts' method provided insight into the distribution of these classes, revealing the number of healthy vs. high-risk loans. This step helps to understand the class imbalance, which is important for model training and evaluation. The data was then split into training and testing sets to build and evaluate the model effectively.

---

### Steps of the Logistic Regression:
- Data Preparation: Features were separated from labels, and the data was split into training and testing sets.
- Model Training: A logistic regression model was fitted using the LogisticRegression function from sklearn.linear_model. This model is ideal for binary classification tasks.
- Prediction and Evaluation: Predictions were made on the test data and compared with actual outcomes. Metrics such as accuracy, precision, and recall were used to evaluate the model's performance.

---

### Results

#### Confusion Matrix:
* **True Negatives:** 18,679
    * Healthy loans correctly identified
* **False Positives:** 80
    * Healthy loans incorrectly identified as high-risk
* **False Negatives:** 67
    * High-risk loans incorrectly identified as healthy
* **True Positives:** 558
    * High-risk loans correctly identified

#### Classification Report:
* **Accuracy:** 99%
* **Precision for healthy loans (0):** 100%
* **Recall for healthy loans (0):** 100%
* **Precision for high-risk loans (1):** 87%
* **Recall for high-risk loans (1):** 89%

---

### Summary 

The logistic regression model is 99% accurate. However, to understand how well the model performed, we need to compare the results for healthy loans (0) versus high-risk loans (1).

The logistic regression model performed perfectly in predicting healthy loans with 100% precision and recall. This is important for the lending services company because it accurately predicts borrowers who are low-risk (healthy loaners).

However, the model achieved 87% precision in predicting high-risk loans, meaning it misclassified 13% of borrowers as high-risk. The recall for high-risk loans is 89%, indicating the model catches most high-risk loans but misses about 11% of the actual high-risk loans. Due to the lower precision and recall scores, there is a potential risk for the lending service company, as there is a chance of misclassifying high-risk borrowers as low-risk.

In general, the accuracy of the model was found to be 99%. This suggests that the model makes very few errors in its classification and provides a high level of reliability in its prediction of healthy versus high-risk loans. However, I do not recommend the logistic regression model despite its high overall accuracy, because the model achieves only 87% precision for high-risk loans, leading to false positives, and its 89% recall indicates it misses 11% of actual high-risk loans. This poses a substantial financial risk to the lending services company, as misclassifying high-risk borrowers as low-risk could lead to increased loan defaults and negatively impact the company's profitability and stability.

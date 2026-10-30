# M.Tech (AIML) Machine Learning - Assignment 2

## a. Problem Statement
The objective of this project is to develop and evaluate an end-to-end predictive framework to classify financial credit risk profile ratings. Using data detailing demographic attributes, transactional relationships, and banking histories, the system implements 5 distinct classification models to accurately distinguish high-risk credit applicants from low-risk individuals.

## b. Dataset Description
* **Dataset Name:** UCI German Credit Dataset
* **Source Repository:** UCI Machine Learning Repository / OpenML (Data ID: 31)
* **Instance Count:** 1,000 instances (Evaluated split sample size: 300 instances)
* **Feature Count:** 20 features (including numerical accounts status, credit durations, history paths, loan purpose, and employment length details)
* **Target Label:** Binary classification (`0` = Negative / Good Credit Risk, `1` = Positive / Bad Credit Risk)

## c. GitHub Repository Link
* **Repository Link:** [INSERT YOUR GITHUB URL HERE]
* **Live Streamlit App:** https://bits-ml.streamlit.app/

## d. Models Used & Performance Evaluation

### Performance Comparison Table

| ML Model Name | Accuracy | AUC | Precision | Recall | F1 | MCC |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| Logistic Regression | 0.7133 | 0.7470 | 0.7562 | 0.8714 | 0.8097 | 0.2505 |
| Decision Tree Classifier | 0.6833 | 0.6773 | 0.7556 | 0.8095 | 0.7816 | 0.2100 |
| K-Nearest Neighbor Classifier | 0.7000 | 0.6747 | 0.7439 | 0.8714 | 0.8026 | 0.2045 |
| Naive Bayes Classifier | 0.7133 | 0.7476 | 0.7981 | 0.7905 | 0.7943 | 0.3218 |
| Support Vector Machine | 0.7133 | 0.7718 | 0.7296 | 0.9381 | 0.8208 | 0.1940 |

### Model Performance Observations
* **Logistic Regression:** Demonstrates balanced optimization stability. It matches the top tier for overall Accuracy (0.7133) and registers a solid F1-Score (0.8097) alongside strong Recall (0.8714), showing stable classification capabilities across linear spaces.
* **Decision Tree Classifier:** Prone to high regional variance partitioning. It exhibits the weakest generalization metrics, scoring the lowest overall Accuracy (0.6833), which highlights an inherent vulnerability to over-fitting on small sample feature boundaries.
* **K-Nearest Neighbor Classifier:** Exhibits lower structural consistency. While distance spatial mapping yields high class recall (0.8714), it suffers from a poor area-under-the-curve index (AUC: 0.6747), meaning it struggles to separate true positive distributions from false positive distributions effectively.
* **Naive Bayes Classifier:** Showcases exceptional class discrimination mechanics. By focusing heavily on conditional probabilities, it establishes the **highest overall Precision (0.7981)** and a commanding **highest MCC score (0.3218)**, meaning it generates the fewest false positive alerts.
* **Support Vector Machine:** Achieves superior hyper-plane separation stability. It registers an outstanding **Recall score of 0.9381**, missing only 13 positive targets across the test block, making it exceptionally reliable at flagging high-risk individuals.

### Overall Winner for the Dataset
**Support Vector Machine (SVM)** is the clear performance winner. It registers the highest discrimination capability across complex non-linear structures (AUC = 0.7718) and achieves the top overall balanced representation score (F1 = 0.8208). By minimizing false negatives down to just 13 occurrences, this model provides the lowest operational liability for credit default risk assessments. 

*(Alternative selection note: If the institutional profile demands minimizing false positives, **Naive Bayes Classifier** serves as a strong choice due to its superior Precision and Matthews Correlation Coefficient).*

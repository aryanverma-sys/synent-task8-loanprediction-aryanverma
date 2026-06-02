# synent-task8-loanprediction-aryanverma
# Task 8: Machine Learning Loan Prediction Model

##  Problem Statement
The objective of this project is to build a high-accuracy classification machine learning model capable of evaluating applicant asset profiles, liabilities, and financial backgrounds to predict whether a loan request should be Approved or Rejected.

##  Dataset Details
* **Source:** Uploaded Loan Approval Dataset
* **Dimensions:** 4,269 entries across 13 columns
* **Target Variable:** `loan_status` (Approved / Rejected)
* **Key Features:** `cibil_score`, `loan_amount`, `loan_term`, `income_annum`, and asset valuations (residential, commercial, luxury, bank).

##  Step-by-Step Approach
1. **Data Cleaning:** Stripped hidden leading whitespaces from column names and string cells to prevent script parsing errors. Removed identifier markers (`loan_id`).
2. **Feature Encoding:** Utilized `LabelEncoder` to convert categorical columns (`education`, `self_employed`, `loan_status`) into numerical variables suitable for machine learning algorithms.
3. **Data Splitting:** Partitioned features and target metrics into an 80% training set and a 20% validation test set using a locked random state for reproducibility.
4. **Model Training:** Implemented and compared both a single Decision Tree Classifier and an ensemble Random Forest Classifier.

##  Key Results & Evaluation
* **Top-Performing Model:** The **Random Forest Classifier** outperformed the standalone decision tree, achieving an overall classification accuracy of **97.78%**.
* **Primary Insight:** Feature importance evaluation revealed that an applicant's **`cibil_score` (Credit Score)** holds over **80%** of the decision-making weight, proving credit history is the single most vital factor in the pipeline.

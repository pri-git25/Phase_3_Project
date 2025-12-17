# Phase_3_Project
# SyriaTel Customer Churn Prediction

## Overview

Customer churn poses a significant financial risk to telecommunications companies. This project applies classification modeling techniques to predict whether a SyriaTel customer is likely to churn (stop doing business with the company). By identifying high-risk customers early, SyriaTel can take proactive retention measures and reduce revenue loss.

## Business and Data Understanding

**Stakeholder:** SyriaTel Management and Customer Retention Teams
**Business Problem:** Customer attrition directly impacts profitability. The objective is to build a predictive model that identifies customers likely to churn so that targeted retention strategies can be deployed.

**Dataset:** The SyriaTel Customer Churn dataset contains customer demographics, usage patterns, service plans, and a binary churn indicator. The target variable is `churn`, where 1 indicates churn and 0 indicates retention.

**Key Challenges:**

* Class imbalance between churned and non-churned customers
* Presence of categorical variables requiring encoding
* Ensuring model interpretability for business stakeholders

## Modeling

An iterative modeling approach was adopted:

1. **Baseline Model – Logistic Regression**
   A simple and interpretable model was built to establish a performance benchmark. Feature scaling and encoding were applied, and recall was emphasized due to the business cost of missing churned customers.

2. **Tuned Model – Decision Tree Classifier**
   A decision tree with tuned hyperparameters was implemented to capture non-linear relationships and improve predictive performance while maintaining interpretability.

Both models were evaluated using the same train-test split to ensure fair comparison.

## Evaluation

Models were assessed using multiple classification metrics:

* Accuracy
* Precision
* Recall (primary metric)
* F1-score
* ROC-AUC

The tuned decision tree outperformed the baseline model, achieving higher recall and better overall balance between identifying churners and minimizing false positives.

## Conclusion and Limitations

**Conclusion:**
The final model demonstrates that customer churn can be reasonably predicted using historical usage and service-related features. The decision tree model is recommended due to its improved recall and transparent decision logic.

**Limitations:**

* The model relies solely on historical data and may not capture sudden behavioral changes
* External factors such as competitor promotions are not included
* Performance may degrade over time without retraining

## Final Recommendation

SyriaTel should deploy the tuned decision tree model as an early-warning system for churn risk. High-risk customers identified by the model should be prioritized for retention campaigns such as personalized offers or service interventions. Regular model retraining and enrichment with additional customer data are advised to sustain performance.

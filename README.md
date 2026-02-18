# sla-breach-prediction
Predicting SLA breaches using early ticket behavior and logistic regression

Problem Statement

Service tickets often breach SLA due to delayed response and inactivity.
This project aims to predict SLA breaches using only the first 48 hours of ticket activity.

The goal is to identify early behavioral signals that indicate high breach risk.

Feature Engineering (First 48 Hours)

From ticket event logs, the following behavioral features were engineered:

Max inactivity gap (48h) – Longest silence period between updates

Average inactivity gap – Mean delay between updates

Update count (48h) – Number of updates in first 48 hours

Time to first update – Initial response delay

These features capture responsiveness and early engagement patterns.

Model Development

Train/Test Split: 70% training / 30% testing

Stratified sampling to maintain class balance

Feature Scaling using StandardScaler

Model: Logistic Regression

Model Development

Train/Test Split: 70% training / 30% testing

Stratified sampling to maintain class balance

Feature Scaling using StandardScaler

Model: Logistic Regression

Model Performance
Metric	Value
ROC-AUC	0.65
Default Recall (Breach)	15%
Optimized Recall (Threshold = 0.35)	51%
Precision at Optimized Threshold	~49%
Accuracy	~63%

Key Insights

Slow time to first response is the strongest predictor of SLA breach.

Large inactivity gaps increase breach probability.

Raw update frequency alone is not a strong predictor.

Early behavioral signals contain meaningful predictive power (AUC = 0.65).

Future Improvements

Implement Random Forest for performance comparison

Add Precision-Recall curve visualization

Perform hyperparameter tuning

Explore full lifecycle feature modeling

Future Improvements

Implement Random Forest for performance comparison

Add Precision-Recall curve visualization

Perform hyperparameter tuning

Explore full lifecycle feature modeling



﻿# AnaomolyDetection

Used AdaBoost with Decision Trees as the base classifier. Before training the model, the data went through a data cleaning process to handle missing values, outliers, and multicollinearity.

Data Cleaning:

Duplicate rows were checked and removed if present.
No missing values were found, so no imputation was required.
No invalid values were found, so no data corrections were needed.
Outliers:

Outliers were not treated because they represent unusual and potentially suspicious activities, which are critical for accurately identifying fraudulent transactions. Removing outliers might result in the loss of important information.
Multi-collinearity:

An extremely high positive correlation of 0.998803 was found between "oldbalanceOrg" and "newbalanceOrig," indicating multicollinearity.
To address multicollinearity, the "newbalanceOrig" column was deleted, along with the "oldbalanceDest," "nameOrig," and "nameDest" columns.
Encoding and Scaling:

One-hot encoding was applied to the "type" column, which likely contained categorical data.
Feature scaling was not performed because it is generally not recommended in fraud detection.
Model Selection and Evaluation:

The dataset was split into training and testing sets with an 80-20 split.
The selected model was AdaBoost with Decision Trees as the base classifier.
The model achieved high accuracy scores, with an accuracy of 1.00 for fraud detection on the test set.
Confusion Matrix:

The confusion matrix for the AdaBoost model was provided, showing the number of True Positives (correctly classified fraud cases), True Negatives (correctly classified non-fraud cases), False Positives (non-fraud cases incorrectly classified as fraud), and False Negatives (fraud cases incorrectly classified as non-fraud).

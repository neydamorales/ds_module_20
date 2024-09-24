# ds_module_20
supervised learning

Overview of the Analysis
The purpose of this analysis to build a model that can identify the creditworthiness of borrowers. The dataset looked at 'loan_size', 'interest_rate', 'borrower_income', 'debt_to_income', 'num_of_accounts', 'derogatory_marks', 'total_debt', and 'loan_status'. The classification model built was expected to predict loan status using the above list as inputs. The dataset showed a significant class imbalance, meaning the number of loans in the healthy category (0) was much larger than those in the risky category (1). When training a machine learning model, this imbalance could affect the model's ability to accurately predict the minority class. Given this imbalance, it would be necessary to use different evaluation metrics (like F1 score) or employ specialized algorithms designed to handle imbalanced datasets. In order to prepare the data for a logistic regression model, the target variable (labels) (or 'loan_status' column) was assigned to y (which was used to train the model), and the feature names were defined as 'loan_size', 'interest_rate', 'borrower_income', 'debt_to_income', 'num_of_accounts', 'derogatory_marks', and 'total_debt' and assigned to X (which were used as inputs to the model). The features (X) and labels (y) were split into training and testing datasets with 25% of the data for testing and 75% for training. The split maintained the same proportion of the target classes ('loan_status') in both the training and testing sets. 
The fit method was applied to the logistic regression model (lr) to train it using the training data (X_train and y_train). The predict method was used to make predictions on the testing data (X_test). The predict_proba method was used to return the probabilities of each class for the testing data. 

Results
Machine Learning - Logistic Regression model: 
True Positives: 593 
True Negatives: 18673 
False Positives: 86 
False Negatives: 32 

The classification report displays how well a model is performing across different classes, especially in cases of class imbalance.

Accuracy: {593 + 18673}/{18673 + 86 + 32 + 593} = ~0.996 - This indicates that the model is correct about 99.6% of the time.
Precision: {593}/{593 + 86} = ~0.874 - This indicates that when the model predicts a positive class, it is correct about 87.4% of the time.
Recall (Sensitivity): {593}/{593 + 32} = ~0.949 - This indicates that the model correctly identifies about 94.9% of the actual positive cases.
F1 Score: 2*{~0.874*~0.949}/{~0.874 + ~0.949} = ~0.909 - This is the harmonic mean of precision and recall, providing a balance between the two metrics.
Support is the number of actual occurrences of each class in the specified dataset.

The confusion matrix indicates that the model performs very well overall, with a high accuracy and good recall. However, the precision is lower, which suggests that while the model is good at identifying true positives, it also has a notable number of false positives.


# PhisBuster

**Objective**

Ever since the emergence of the Internet, phishing, a fraudulent practice, has always been an area of concern. We have approached this problem via machine learning. Through this project, we compare many supervised machine learning algorithms on a publicly available dataset that has an equal number of phishing and legitimate URLs, and we have identified a model that effectively classifies whether a given URL is a phishing site or not.

**Data Collection**

For training and testing machine learning algorithms, we have used a huge dataset of 651,191 URLs, out of which 428103 benign or safe URLs, 96457 defacement URLs, 94111 phishing URLs, and 32520 malware URLs. 
Dataset Link:https://www.kaggle.com/datasets/sid321axn/malicious-urls-dataset?resource=download

**Feature Engineering**

We extracted a few domain-based features and address bar features for the URLs in the base dataset. A decision tree was applied to this data to obtain the feature importance, and the unnecessary features were deleted from the dataset. This data was further split for training and testing.

Based on the dataset, the values of each feature were converted to 0 for a legitimate site and 1 for a phishing site. The respective feature extraction process is in 'feature_extraction.py'.

This new dataset is available in 'phishing_feature_engg.csv' of this repository.

**Model Development**

The supervised machine learning algorithms used for this analysis are:

- Logistic Regression
- Naive Bayes Classifier
- Decision Tree Classifier
- Random Forest Classifier
- XGBoost Classifier

These models were trained and tested on the feature-extracted dataset, and evaluations were done to identify the model with high performance. The XGBoost algorithm had good accuracy and a fast testing time compared to the other algorithms. Later, a grid search was done on the XGBoost for hyperparameter tuning.

**Results**

After fine-tuning, the XGBoost classifier was chosen as the final model with an accuracy of 82.4%. This model was saved as the final model through the pickle module of Python. This file is available as 'phishing_classifier.pkl'.

**Future Work**

The saved model can be extended to a browser extension or can be added as a plugin to internet security providers to warn users and help them avoid phishing sites by efficiently identifying them.

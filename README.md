# Project Overview
This was a group project where we built a machine learning pipeline to predict whether the bonding process of aerogel materials would be successful. We cleaned a raw dataset, explored the data with visual graphs, and trained three different classification models to see which one performed the best.

# Tools Used

Programming: Python

Data & Math Libraries: pandas, numpy

Machine Learning: scikit-learn (Logistic Regression, Decision Trees, Random Forest, GridSearchCV)

Visualization: matplotlib, seaborn

# The Process

1. Data Preparation and Exploration
We started by cleaning the dataset. We filled missing numbers using the median value and filled missing text categories with the most common value. We then used graphs (histograms, boxplots, and scatter plots) to understand the age range of applicants and how different job statuses related to bonding risk. Finally, we converted categorical data into numbers using one-hot encoding and scaled the data so it was ready for the algorithms.

2. Model Training and Testing
We split our data into training (70%), validation (20%), and testing (10%) sets. We tested three different algorithms to predict the target variable (BondingSuccessful):

Logistic Regression: We trained a baseline model and created a bar chart of the coefficients to see which features had the biggest impact on bonding success.

Decision Tree (CART): We trained a tree model and visualized the actual splits to understand how the model was making its decisions.

Random Forest: We trained an ensemble model, which achieved a 95% accuracy and a 0.99 ROC-AUC score on the validation set.

3. Hyperparameter Tuning
To make our models even better, we used GridSearchCV with 5-fold cross-validation on both the Decision Tree and the Random Forest. We tested multiple parameters (like max_depth and n_estimators) and optimized the models specifically for the F1-score, which helps balance precision and recall.

# Key Results

All models were evaluated using confusion matrices, precision/recall scores, and ROC-AUC curves to ensure they could accurately separate successful bonding from unsuccessful bonding.

The Random Forest model proved to be highly robust, showing consistent performance between the validation and test sets.

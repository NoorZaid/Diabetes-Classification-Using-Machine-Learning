# 🩺 Diabetes Classification Using Machine Learning

A machine learning classification project using the **Scikit-learn
Diabetes dataset** to classify observations into **Low** and **High**
target groups. The project trains and compares Decision Tree and Random
Forest classifiers and explores feature importance.

## 📌 Project Overview

This notebook uses the built-in Diabetes dataset from Scikit-learn. The
original target is converted into a binary classification label using
the target mean as the threshold:

-   `0` = Low (target value less than or equal to the mean)
-   `1` = High (target value greater than the mean)

A Decision Tree Classifier and a Random Forest Classifier are trained
using the same train/test split. Their performance and feature
importance are then examined.

## 🎯 Project Objectives

-   Load and prepare the Scikit-learn Diabetes dataset.
-   Convert the original numerical target into two classes.
-   Split the data into training and testing sets.
-   Train a Decision Tree classification model.
-   Train a Random Forest classification model.
-   Evaluate the Decision Tree using a confusion matrix, classification
    report, and accuracy.
-   Identify important features using Gini importance and permutation
    importance.
-   Compare the accuracy and confusion matrices of both models.

## 📂 Dataset

**Dataset:** Diabetes dataset (built into Scikit-learn)

**Source:** [Scikit-learn --
`load_diabetes`](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_diabetes.html)

The notebook loads the dataset directly with
`sklearn.datasets.load_diabetes()`. It uses the dataset's feature
columns as predictors and transforms the numerical target into binary
labels using its mean.

## 🛠️ Technologies & Libraries

-   Python
-   Pandas
-   NumPy
-   Scikit-learn
-   Matplotlib
-   Seaborn

## 🔍 Project Workflow

### 1. Load & Prepare the Data

-   Load the Diabetes dataset using Scikit-learn.
-   Store the input features in a Pandas DataFrame.
-   Convert the continuous target into binary classes using the mean
    target value.
-   Display sample features and the first binary labels.

### 2. Train/Test Split

The dataset is divided into:

-   Training set: 75%
-   Testing set: 25%
-   `random_state`: 1

### 3. Decision Tree Classifier

-   Initialize a `DecisionTreeClassifier` with `random_state=1`.
-   Train the model using the training data.
-   Predict the classes for the test data.

### 4. Decision Tree Evaluation

Evaluate the Decision Tree model using:

-   Confusion matrix.
-   Classification report.
-   Accuracy score.
-   Confusion matrix heatmap.

### 5. Random Forest Classifier

Train a `RandomForestClassifier` with:

-   Number of trees: 150
-   `random_state`: 1

Use the trained model to predict the test labels.

### 6. Feature Importance -- Gini Index

Extract the Random Forest model's built-in `feature_importances_`
values, organize them in a DataFrame, and plot the features in
descending order of Gini importance.

### 7. Permutation Importance

Calculate permutation importance on the test set using:

-   `n_repeats`: 30
-   `random_state`: 42

Plot the mean permutation importance for each feature.

### 8. Model Comparison

Compare the Decision Tree and Random Forest models using:

-   Accuracy scores.
-   Confusion matrices.
-   Side-by-side confusion matrix visualizations.

## 📊 Expected Outputs

-   Preview of the dataset features and binary labels.
-   Decision Tree confusion matrix and classification report.
-   Decision Tree accuracy score.
-   Gini feature-importance chart.
-   Permutation feature-importance chart.
-   Accuracy comparison between Decision Tree and Random Forest.
-   Side-by-side confusion matrices.

*The notebook source does not include fixed result values, so
performance metrics should be added after running the notebook.*

## 🚀 How to Run the Project

1.  Open the notebook in Jupyter Notebook or Google Colab.
2.  Install the required libraries if they are not already available.
3.  Run the notebook cells from top to bottom.
4.  Review the classification metrics, feature-importance plots, and
    model comparison.

## 📁 Repository Structure

``` text
Diabetes-Classification/
│
├── README.md
└── diabetes.ipynb
```

## ⚠️ Important Note

This notebook uses the Scikit-learn Diabetes dataset and converts its
continuous target into Low/High groups for a classification exercise.
This is a machine learning demonstration, **not a clinical diabetes
diagnosis or a validated medical prediction system**.

------------------------------------------------------------------------

**Project Focus:** Machine Learning \| Classification \| Decision Tree
\| Random Forest \| Feature Importance

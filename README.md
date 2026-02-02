# 📊 Sampling Techniques on Imbalanced Credit Card Dataset

##  Introduction
In many real-world machine learning problems, datasets are imbalanced, meaning one class has significantly more samples than the other. This imbalance can lead to biased models and poor prediction performance.

The main objective of this assignment is to understand how different sampling techniques affect the performance of various machine learning models when applied to an imbalanced credit card transaction dataset.

---

##  Dataset Description
The dataset used in this project is a credit card transaction dataset where:
- Class `0` represents non-fraudulent transactions
- Class `1` represents fraudulent transactions

Initially, the dataset was highly imbalanced, with very few fraudulent transactions compared to non-fraudulent ones.  
The dataset was uploaded manually to Google Colab and all experiments were performed in the Colab environment.

---

##  Handling Imbalanced Data
To handle the imbalance in the dataset, random undersampling was applied:
- The majority class (non-fraudulent transactions) was downsampled
- The minority class (fraudulent transactions) was kept unchanged

This resulted in a balanced dataset, which helps machine learning models learn patterns from both classes more effectively.

---

##  Sampling Techniques Used
Five sampling techniques were implemented as part of this assignment:

###  Simple Random Sampling
- Samples were selected randomly from the balanced dataset
- It is easy to implement but may not always preserve class proportions

###  Stratified Sampling
- Ensures that both classes are equally represented in the training data
- Particularly effective for imbalanced datasets
- Produces more stable and reliable results

###  Systematic Sampling (Interval-based)
- Samples were selected at fixed intervals from the dataset
- Simple and structured approach to sampling

###  Bootstrap Sampling
- Sampling was performed with replacement
- Useful for improving model stability and handling smaller datasets

###  Cross-Validation Sampling (Stratified K-Fold)
- The dataset was divided into multiple folds
- Each fold maintained class balance
- Provides a reliable estimate of model performance

Cluster sampling was not used because the dataset does not contain natural clusters such as geographical regions or branches.

---

##  Machine Learning Models Used
The following five machine learning models were trained and evaluated:

| Model ID | Algorithm |
|--------|----------|
| M1 | Logistic Regression |
| M2 | Decision Tree |
| M3 | Random Forest |
| M4 | K-Nearest Neighbors (KNN) |
| M5 | Support Vector Machine (SVM) |

---

##  Results and Accuracy Comparison
Each model was trained using all five sampling techniques.  
Accuracy was calculated for every combination of model and sampling method, and the results were compared using an accuracy table.

The comparison shows that the choice of sampling technique has a significant impact on model performance.

---

##  Observations
- Stratified Sampling performed well for most models
- Stratified K-Fold Cross-Validation provided consistent and stable accuracy
- Simple and systematic sampling showed higher variation in performance
- Proper sampling is crucial when dealing with imbalanced datasets

---

##  Conclusion
This assignment demonstrates that sampling techniques play a vital role in improving machine learning model performance on imbalanced datasets. Among all the methods used, Stratified Sampling and Cross-Validation proved to be the most effective and reliable.

This experiment helped in understanding the practical importance of sampling in real-world machine learning problems.

---


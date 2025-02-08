# Machine Learning Algorithms Evaluation

## Overview
This project evaluates and compares multiple machine learning models on the **Breast Cancer Dataset**. The objective is to analyze their performance based on key classification metrics and hyperparameter tuning.

The models implemented include:
- **K-Nearest Neighbors (KNN)**
- **Logistic Regression**
- **Support Vector Machines (SVM)**
- **Ensemble Methods**: Boosting (AdaBoost) and Bagging (Random Forest)

## Dataset
The **Breast Cancer Dataset** contains 569 samples with 30 numerical features derived from geometric properties of breast mass images. The dataset was split into **training (75%)** and **testing (25%)** sets, with features standardized by removing the mean and scaling to unit variance.


## Model Implementations
### 1. K-Nearest Neighbors (KNN)
- Experimented with **various distance metrics**: Euclidean, Manhattan, and Cosine.
- Tuned **number of neighbors** (K) using cross-validation.
- Achieved **96% accuracy** with **Cosine distance and K=5**.

### 2. Logistic Regression
- Evaluated **L1 (Lasso) and L2 (Ridge) regularization**.
- Performed **grid search** to optimize regularization strength (C).
- Achieved **97% accuracy** with **L2 regularization (C=1)**.

### 3. Support Vector Machines (SVM)
- Experimented with different **kernels**: Linear, Polynomial, RBF, and Sigmoid.
- Tuned **C values** via cross-validation.
- Achieved **97% accuracy** with **Linear Kernel (C=0.2)**.

### 4. Ensemble Methods
#### **Boosting - AdaBoost**
- Evaluated different **learning rates and number of estimators**.
- Best performance with **1100 estimators and learning rate = 1.5**.
- Achieved **97% accuracy and AUC of 0.995**.

#### **Bagging - Random Forest**
- Tuned **number of estimators, max features, and max depth**.
- Best performance with **80 estimators, max depth=5, and max features=log2**.
- Achieved **97% accuracy and AUC of 0.996**.

## Performance Comparison
| Model                | Precision | Recall | F1-Score | Accuracy | AUC  |
|----------------------|-----------|--------|----------|----------|------|
| **KNN**              | 0.98      | 0.96   | 0.97     | 0.96     | 0.985 |
| **Logistic Regression** | 0.99   | 0.98   | 0.98     | 0.97     | 0.997 |
| **SVM**              | 0.98      | 0.98   | 0.98     | 0.97     | 0.997 |
| **Random Forest**    | 0.97      | 0.98   | 0.97     | 0.97     | 0.996 |
| **AdaBoost**         | 0.99      | 0.97   | 0.98     | 0.97     | 0.995 |

## Conclusion
- **Logistic Regression** provided the best performance across all metrics.
- **SVM and Random Forest** also performed well with high accuracy and AUC scores.
- **Ensemble methods (AdaBoost and Random Forest)** demonstrated robust results, leveraging multiple weak learners for improved accuracy.
- The **KNN model**, while effective, was slightly less optimal compared to other classifiers.


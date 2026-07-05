# Student Dropout and Academic Success Prediction with Machine Learning

This project focuses on predicting students' academic outcomes using machine learning classification algorithms. The dataset includes demographic, academic, socio-economic, and enrollment-related features. The target variable consists of three student outcome classes: Dropout, Enrolled, and Graduate.

## Project Objective

The main objective of this project is to compare different machine learning algorithms and evaluate their performance on student academic success prediction. This type of classification problem can be useful for identifying students who may be at risk of dropping out and supporting data-driven decision-making in educational institutions.

## Dataset Overview

The dataset contains 4,424 records and 37 columns. The target column is `Target`, which includes the following classes:

* Dropout
* Enrolled
* Graduate

For model training, the target labels were encoded numerically:

* Dropout: 0
* Enrolled: 1
* Graduate: 2

Some non-numeric or problematic columns were removed before training to make the dataset suitable for machine learning models.

## Machine Learning Models Used

The following classification algorithms were implemented and compared:

* Naive Bayes
* K-Nearest Neighbors
* Decision Tree
* Support Vector Machine
* Multi-Layer Perceptron
* Random Forest
* XGBoost

## Evaluation Metrics

The models were evaluated using K-Fold Cross Validation with 5 and 10 folds. The following metrics were used:

* Accuracy
* Precision
* Recall
* F1-score
* Cohen’s Kappa

## Results Summary

Random Forest and XGBoost achieved the strongest results among the tested models.

| Model         | K-Fold | Accuracy | Precision | Recall | F1-score | Cohen’s Kappa |
| ------------- | -----: | -------: | --------: | -----: | -------: | ------------: |
| Random Forest |      5 |   0.7780 |    0.7663 | 0.7780 |   0.7627 |        0.6232 |
| XGBoost       |     10 |   0.7749 |    0.7653 | 0.7749 |   0.7625 |        0.6196 |
| SVM           |      5 |   0.7609 |    0.7436 | 0.7609 |   0.7408 |        0.5905 |
| MLP           |     10 |   0.7256 |    0.7178 | 0.7256 |   0.7197 |        0.5471 |
| K-NN          |      5 |   0.7016 |    0.6820 | 0.7016 |   0.6877 |        0.4987 |
| Decision Tree |     10 |   0.6738 |    0.6800 | 0.6738 |   0.6759 |        0.4728 |
| Naive Bayes   |     10 |   0.6702 |    0.6519 | 0.6702 |   0.6580 |        0.4473 |

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Jupyter Notebook

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/student-dropout-ml-classification.git
```

2. Install the required libraries:

```bash
pip install -r requirements.txt
```

3. Open the notebook:

```bash
jupyter notebook notebooks/ML_Proje.ipynb
```

4. Run all cells in the notebook.

## Future Improvements

* Use Stratified K-Fold Cross Validation for better class distribution handling.
* Add machine learning pipelines to avoid data leakage during scaling.
* Perform hyperparameter tuning with GridSearchCV or RandomizedSearchCV.
* Add visualizations such as confusion matrix and feature importance plots.
* Convert the notebook into a clean Python script structure.
* Deploy a simple Streamlit interface for prediction.

## Project Status

Initial machine learning benchmark completed. Future versions will focus on improving model reliability, visualization, and deployment.

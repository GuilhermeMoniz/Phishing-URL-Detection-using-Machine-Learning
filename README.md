# Phishing URL Detection using Machine Learning

This project develops a machine learning pipeline to detect phishing URLs using the PhiUSIIL Phishing URL Dataset. The workflow covers data cleaning, feature preprocessing, correlation analysis, statistical feature selection, dimensionality reduction, class balancing, model comparison, and hyperparameter tuning.

## Dataset

The project uses the PhiUSIIL Phishing URL Dataset, which contains 235,795 labeled URLs and 55 features extracted from URL structure and webpage HTML. After removing duplicated rows and excluding categorical columns, the working dataset contained only numerical features for model training.

## Methodology

The preprocessing pipeline included:
- Duplicate removal and missing-value checking.
- Min-Max scaling to normalize feature ranges.
- Pearson correlation analysis to remove redundant variables.
- Kruskal-Wallis testing to select statistically significant features.
- PCA and LDA for dimensionality reduction.
- Random oversampling and undersampling to address class imbalance.

## Models

The following classifiers were implemented and evaluated:
- Minimum Distance Classifier with Euclidean distance.
- Minimum Distance Classifier with Mahalanobis distance.
- Fisher-LDA.
- K-Nearest Neighbors.
- Gaussian Naive Bayes.
- Support Vector Machine.

## Results

The models were evaluated with stratified 5-fold cross-validation using accuracy, F1-score, sensitivity, specificity, and ROC-AUC. LDA consistently produced better class separation than PCA, and the strongest models achieved near-perfect results on this dataset. Hyperparameter tuning further confirmed that the dataset is highly separable and that SVM and KNN perform especially well.
## Repository Structure

- `notebook/` — main exploratory and modeling notebook.
- `report/` — final project report.
- `data/` — raw dataset placeholder

## Tools

Python, Pandas, NumPy, Scikit-learn, Imbalanced-learn, Matplotlib, Seaborn, SciPy.

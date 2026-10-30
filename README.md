# Cancer Variant Prioritization Using Machine Learning

### Machine Learning | Bioinformatics | Cancer Genomics | Python

## Overview

Cancer Variant Prioritization Using Machine Learning is a bioinformatics project that applies supervised machine learning to predict the clinical significance of genetic variants associated with cancer.

The project uses a Random Forest classification model and genomic variant features to classify variants according to their recorded clinical significance. It combines data preprocessing, categorical encoding, model training, performance evaluation, and feature-importance analysis in a reproducible machine learning workflow.

The project demonstrates how machine learning techniques can be applied to genomic data analysis and computational approaches to variant prioritization.

## Objectives

- Develop a machine learning classification pipeline for cancer-associated genetic variants.
- Process numerical and categorical genomic features.
- Train a Random Forest classifier to predict clinical significance.
- Evaluate classification performance using standard machine learning metrics.
- Examine feature importance to understand which input variables contribute to model predictions.
- Explore the application of data science techniques to bioinformatics.

## Dataset

The dataset contains **10,000 records and 9 columns**, including genomic variant information and clinical significance labels.

### Features

| Feature | Description |
|---|---|
| Chromosome | Chromosome associated with the variant |
| Position | Genomic position of the variant |
| Gene | Gene associated with the variant |
| Variant_Type | Type of genetic variant |
| Population_AF | Population allele frequency |
| CADD_Score | Variant deleteriousness score |
| SIFT | Functional prediction annotation |
| PolyPhen | Protein-impact prediction annotation |
| Clinical_Significance | Target variable for classification |

The `Clinical_Significance` column is encoded for supervised classification.

**Note:** The dataset's provenance and the biological validity of its annotations should be verified before drawing scientific conclusions.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Pickle
- Jupyter Notebook

## Machine Learning Workflow

### 1. Data Loading and Exploration
Load the dataset and inspect its columns and structure.

### 2. Data Preprocessing
- Impute missing numerical values using column means.
- Impute missing categorical values using column modes.
- Encode the target labels.
- Identify numerical and categorical input features.

### 3. Feature Transformation
- Apply `StandardScaler` to numerical features.
- Apply `OneHotEncoder` to categorical features.
- Combine transformations using Scikit-learn's `ColumnTransformer`.

### 4. Train-Test Split
Split the dataset into training and testing subsets using an 80:20 ratio and a fixed random state.

### 5. Model Training
Train a Random Forest classifier with the following configuration:

- Number of estimators: 200
- Maximum tree depth: 10
- Random state: 42

The preprocessing and classifier are combined into a Scikit-learn pipeline.

### 6. Model Evaluation
Evaluate predictions using:

- Accuracy
- Confusion matrix
- Precision
- Recall
- F1-score

### 7. Feature Importance
Extract feature-importance scores from the trained Random Forest model to identify influential input features.

### 8. Model Export
Save the trained preprocessing and classification pipeline as a serialized Pickle file for potential reuse.

## Project Structure

```text
cancer-variant-prioritization-ml/
│
├── First1.ipynb
├── cancer_variant_prioritization_dataset.csv
├── cancer_classification_model.pkl
├── requirements.txt
├── .gitignore
└── README.md
```

## Installation and Usage

### Prerequisites
- Python 3.10 or a compatible Python version
- Jupyter Notebook
- pip

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/cancer-variant-prioritization-ml.git
cd cancer-variant-prioritization-ml
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the notebook

```bash
jupyter notebook First1.ipynb
```

Execute the notebook cells sequentially to explore the dataset, train the model, evaluate its predictions, and inspect feature importance.

## Model Evaluation

The notebook calculates accuracy, a confusion matrix, and a classification report containing precision, recall, and F1-score.

Actual performance metrics should be reported only after running the notebook and verifying the results.

Accuracy alone may not adequately describe performance when clinical-significance classes are imbalanced. Per-class metrics and a comparison with appropriate baselines are also important.

## Limitations

- Predictions depend on the quality and representativeness of the dataset.
- The model's generalization to independent genomic datasets has not been established.
- Feature importance does not establish causality or biological significance.
- Clinical validity and external validation have not been demonstrated.
- The current implementation is an experimental machine learning workflow, not a validated clinical prediction system.

## Responsible Use

This project is intended for educational and research exploration of machine learning in bioinformatics.

**Predictions must not be used to diagnose cancer, determine treatment, or make clinical decisions.** Clinical interpretation of genetic variants requires validated evidence, appropriate reference databases, and qualified professional assessment.

## Future Improvements

- Add cross-validation and hyperparameter optimization.
- Evaluate class imbalance and compare suitable classification baselines.
- Add ROC-AUC or precision-recall analysis where appropriate.
- Test the model on an independent, well-documented dataset.
- Improve data provenance and preprocessing documentation.
- Develop an interactive interface for exploring predictions and evaluation metrics.

## Author

**Aditi Singh**

AI/ML | Computer Science | Data Science | Research Interests in Intelligent Systems

GitHub: https://github.com/its-aditisingh

---

*An exploratory machine learning project at the intersection of artificial intelligence and bioinformatics.*

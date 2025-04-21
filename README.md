# 🚗 Car Acceptability Classification using LDA

Author: Edward Henriquez

Data Science Undergraduate @ University of Georgia

This project uses **Linear Discriminant Analysis (LDA)** to classify cars based on their acceptability levels (unacceptable, acceptable, good, very good) using the [UCI Car Evaluation Dataset](https://archive.ics.uci.edu/dataset/19/car+evaluation).

The goal is to evaluate LDA’s ability to handle categorical data (after preprocessing), explore class separation, and compare its performance to logistic regression — especially under class imbalance.

---

## 📁 Project Structure

```bash
car-acceptability-lda/
├── data/               # Raw and processed datasets
├── notebooks/          # Jupyter notebooks (EDA, modeling, evaluation)
├── report/             # Final report
├── requirements.txt    # Python dependencies
└── README.md           # This file
```

## 🧠 Methods & Tools

Linear Discriminant Analysis (LDA)

Logistic Regression (baseline)

SMOTE (to address class imbalance)

Python, scikit-learn, pandas, seaborn, matplotlib

## 📊 Key Findings

Without resampling, LDA and Logistic Regression both performed well on dominant classes but poorly on minority ones.

Applying SMOTE improved class balance significantly, leading to better macro-F1 scores.

Logistic Regression had a slight performance edge, but LDA still performed competitively and offered interpretable discriminant axes.

## 🧪 How to Run

This project is for academic analysis and is structured for clarity. You can explore the process step-by-step via the notebooks:

notebooks/01_preprocessing.ipynb — Load and encode the dataset

notebooks/02_lda_model.ipynb — Train and evaluate LDA & Logistic Regression

## 📌 Dataset

Bohanec, M. (1988). Car Evaluation [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5JP48.

6 categorical features: buying, maint, doors, persons, lug_boot, safety

1 target variable: car acceptability (4 classes)

```

```

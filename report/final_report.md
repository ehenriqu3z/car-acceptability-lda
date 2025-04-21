# Final Report

Project Summary: LDA for Car Acceptability Classification

Objective: In this project, we applied Linear Discriminant Analysis (LDA) to classify cars based on their acceptability using the UCI Car Evaluation dataset. The target classes were: unacceptable, acceptable, good,
very good.

Our goals were to:

- Preprocess categorical data for LDA,
- Train an LDA classifier to predict acceptability,
- Evaluate its performance, and
- Compare LDA to an alternative model (Logistic Regression),
- Analyze feature impact and class separability.

Methods & Preprocessing:
We used the UCI Car Evaluation dataset (6 categorical features + 1 target class). Since LDA requires numerical input, we applied label encoding to all features. We split the data into training (70%) and test (30%) sets.

Due to class imbalance (most samples were “good”), we:

- Evaluated model performance pre- and post-resampling.
- Applied SMOTE (Synthetic Minority Oversampling Technique) to the training data.

Models Trained:

- LDA (Linear Discriminant Analysis): Generative model using class distributions and shared covariance.
- Logistic Regression: A discriminative, linear baseline for comparison.

Key takeaways:

- Without SMOTE, both models heavily favored the dominant class (“good”).
- With SMOTE, both models achieved more balanced recall across all classes, especially “very good”.
- LDA’s performance was competitive with logistic regression, though logistic regression slightly outperformed it in post-SMOTE balance.
- Accuracy dropped after SMOTE, but macro-average F1 (a fairer metric for imbalance) improved.

Why We Used SMOTE
LDA assumes equal prior probabilities unless specified — this assumption failed under class imbalance. By resampling the training data using SMOTE, we exposed the model to more examples from minority classes, improving its ability to recognize rare but important categories like “acceptable” and “very good.”

Questions?

1. Can LDA differentiate between car acceptability categories?

- Partially. LDA was able to classify dominant classes like “good” accurately, but struggled with rare classes until SMOTE was applied.

2. Which features are most influential?

- persons and lug boot contributed the most.

3. How does LDA compare to another classifier like logistic regression?

- Comparable. Logistic regression had slightly better macro-F1 post-SMOTE, but LDA held up well.

4. What insights can we draw about car evaluation patterns?

- “Good” dominates acceptability judgments — suggesting many cars share mid-level features. Safety and buying price likely contribute to class separation (can be explored through LDA component weights).

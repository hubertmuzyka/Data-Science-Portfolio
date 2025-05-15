# Project: Football Match Result Prediction (W/D/L)

## Project Description

The goal of this project is to investigate and compare the effectiveness of a wide range of machine learning algorithms in the task of predicting football match results (Win - W, Draw - D, Loss - L). The analysis focuses on match data from the German Bundesliga spanning the seasons 2013–2023, enhanced with advanced statistical metrics provided by Understat (including expected goals (xG), expected goals against (xGA), opponent pressing intensity in own half (PPDA), and others). Project was a part of my Master Thesis during Master studies in Warsaw School of Economics (SGH).

The project addresses a **multi-class classification** problem, where each instance (match) is assigned to one of three outcome classes.

## Project Scope

* **Problem Type:** Multi-class Classification (Win, Draw, Loss)
* **Data:** German Bundesliga matches from the 2013–2023 seasons, statistical data from Understat (xG, xGA, PPDA, etc.).
* **Algorithms Tested:** A total of 48 different machine learning models, including:
    * Linear Models: Logistic Regression, Linear Discriminant Analysis (LDA).
    * Support Vector Machines: Support Vector Classification (SVC).
    * Tree-based Models: Random Forest, Gradient Boosting (e.g., LightGBM).
    * Neural Networks: Multi-layer Perceptron (MLPClassifier).
* **Feature Sets:**
    * **Full Feature Set:** Utilizing all available statistical variables.
    * **Reduced Feature Set:** Selected based on conducted statistical tests to identify the most significant predictors.
* **Model Evaluation:**
    * Accuracy
    * F1 Score (macro)
    * Brier Score
* **Data Split:**
    * **Training Set:** Data from seasons prior to 2023.
    * **Test Set:** Data from the 2023 season.
* **Validation:** In-depth statistical analysis of input data and prediction results using tests such as:
    * Kolmogorov–Smirnov test
    * Spearman's rank correlation coefficient
    * Variance Inflation Factor (VIF)
    * Kruskal–Wallis test followed by Dunn's post-hoc test.

## Results

The experiments conducted revealed that the best-performing models included:

* Linear Discriminant Analysis (LDA)
* Support Vector Classification (SVC)
* Multi-layer Perceptron (MLPClassifier)
* LightGBM

Boosting models (including LightGBM) demonstrated good probabilistic calibration, reflected in a low Brier Score. However, they achieved slightly lower macro F1 scores compared to other top-performing models, partly due to the difficulty in predicting the "draw" class.

Simpler models, such as Naive Bayes and Perceptron, performed significantly worse than more complex algorithms.

## Project Goal

The primary goal of this project was to conduct a systematic comparison of a broad spectrum of machine learning algorithms in the context of football match result prediction. By analyzing different models and feature engineering strategies, the project aimed to identify the most effective approach for modeling and predicting match outcomes in sports analytics. These findings can provide valuable insights for further research in the field of football analytics and predictive modeling in sports.
 

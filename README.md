# tb-treatment-outcome-prediction
# Comparative Analysis of Machine Learning Models for Predicting Pulmonary Tuberculosis Treatment Outcomes

A machine learning research project comparing four classification models to predict pulmonary tuberculosis (TB) treatment outcomes using clinical data from Chiang Mai, Thailand.

**Achievement:** **1st Place, Oral Presentation** — The 12th National Conference on Science and Technology, Krung Kao Rajabhat University (12th KKR-NCST), 2026.

---

## Overview

Pulmonary tuberculosis remains a major public health challenge. Identifying patients at risk of unfavorable treatment outcomes can help healthcare professionals prioritize follow-up and allocate healthcare resources more effectively.

This project develops and compares four machine learning and neural network models to classify pulmonary TB treatment outcomes into two categories: favorable and unfavorable.

The study focuses on identifying a suitable predictive model based on multiple evaluation metrics, with the goal of supporting future clinical decision-support research.

## Research Objectives

- Develop predictive models for pulmonary TB treatment outcomes.
- Compare the performance of XGBoost, Random Forest, CatBoost, and Artificial Neural Network (ANN).
- Evaluate model performance using Accuracy, Precision, Recall, and F1-score.
- Identify the model with the strongest overall classification performance.

## Dataset

The study uses clinical records of pulmonary tuberculosis patients within the jurisdiction of the Department of Disease Control Office 1, Chiang Mai Province.

- **Dataset size reported in the study:** 25,239 records
- **Prediction task:** Binary classification
- **Training and testing split:** 80:20

### Target Classes

- **Class 0 — Favorable Outcomes:** Cured and treatment completed.
- **Class 1 — Unfavorable Outcomes:** Death, lost to follow-up, treatment failure, diagnosis changed, and RR/MDR before the fifth month.

### Features

The study considers clinical and demographic variables, including:

- Gender, age, and BMI
- HIV status and comorbidities
- Diabetes mellitus and liver disease
- Chronic kidney disease and chronic obstructive pulmonary disease
- TB follow-up status and cohort
- First-month AFB result
- Patient registration type
- Site of tuberculosis
- Treatment duration

## Methodology

The project follows a machine learning workflow:

1. **Data preprocessing** — Prepare the dataset, encode categorical variables, and handle missing values.
2. **Target construction** — Group treatment outcomes into favorable and unfavorable classes.
3. **Feature selection** — Select the input variables used for prediction.
4. **Data splitting** — Divide the dataset into training and testing sets.
5. **Model training and optimization** — Train and tune the candidate models.
6. **Model evaluation** — Compare classification performance using multiple metrics.

### Models Compared

| Model | Description |
|---|---|
| XGBoost | Gradient boosting with sequential decision trees |
| Random Forest | Ensemble learning using multiple decision trees |
| CatBoost | Gradient boosting designed to handle categorical data effectively |
| Artificial Neural Network (ANN) | Neural network for learning nonlinear patterns |

The workflow also explores class-imbalance handling and hyperparameter optimization.

## Results

The following results are taken from the Notebook's model comparison on the test set of 4,659 records. Precision, Recall, and F1-score in this table use **macro averaging**.

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| XGBoost | 93.97% | 92.08% | 89.58% | 90.75% |
| Random Forest | 93.78% | 91.53% | 89.60% | 90.52% |
| CatBoost | 93.88% | 91.86% | 89.56% | 90.64% |
| ANN | 92.53% | 88.80% | 89.03% | 88.91% |

*Note: Values are rounded to two decimal places.*

### Key Findings

- **XGBoost achieved the highest overall performance** among the four models according to the Notebook's comparison.
- XGBoost achieved an accuracy of approximately 93.97% and a macro F1-score of approximately 90.75%.
- The performance differences among XGBoost, Random Forest, and CatBoost were relatively small.
- Evaluating multiple metrics provides a more informative comparison than relying on accuracy alone, particularly when predicting unfavorable treatment outcomes.

## Technology Stack

- **Programming Language:** Python
- **Data Processing:** Pandas, NumPy
- **Machine Learning:** Scikit-learn, XGBoost, CatBoost
- **Deep Learning:** TensorFlow / Keras
- **Data Visualization:** Matplotlib, Seaborn
- **Model Evaluation:** Classification Report, Confusion Matrix, ROC Curve, Precision–Recall Curve

## Repository Structure

```text
tb-treatment-outcome-prediction/
├── README.md
├── notebooks/
│   └── TB_Classification.ipynb
├── presentation/
│   └── presentation.pdf
└── docs/
    └── abstract.pdf
```

*The structure above describes the intended organization. Only files that are actually uploaded and approved for public release should be included.*

## Research Achievement

**1st Place, Oral Presentation**

The 12th National Conference on Science and Technology, Krung Kao Rajabhat University (12th KKR-NCST), 2026.

This recognition reflects the research and presentation of a comparative machine learning study on pulmonary tuberculosis treatment outcome prediction.

## Limitations and Future Work

This project is a research prototype and is not a clinically validated diagnostic or treatment tool.

Potential future work includes:

- Evaluating the models on independent external datasets.
- Assessing model calibration and generalizability across patient populations.
- Investigating performance for the unfavorable-outcome class in greater depth.
- Improving interpretability to support clinical review.
- Evaluating the model prospectively before considering any real-world clinical application.

## Ethical Considerations

The project involves sensitive healthcare data. Patient-level data, identifiable information, and restricted datasets should not be published in this repository without appropriate authorization.

The public repository should contain only code, documentation, and research outputs that are permitted for public release.

## Disclaimer

This project was developed for academic research and educational purposes. Predictions should not be used as a substitute for professional medical judgment or clinical decision-making.

---

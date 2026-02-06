# financial-data-regression-modeling
Applied statistical modeling for credit risk classification with a focus on feature diagnostics, interpretability, and model behavior under class imbalance.

---

## Overview

This project applies logistic regression–based modeling to borrower-level
financial data to analyze default risk.  
Rather than focusing solely on metric optimization, the emphasis is on
**diagnosing why baseline models fail** and identifying features with genuine
predictive signal.

The workflow reflects a realistic modeling process used in credit risk and
financial analytics.

---

## Key Techniques

- Logistic regression modeling
- AIC-based forward stepwise feature selection
- Missing value imputation (MICE)
- Model diagnostics under class imbalance
- Odds ratio–based interpretability
- Feature-focused experimentation

---

## Modeling Workflow

1. **Data preprocessing**
   - Categorical encoding
   - MICE imputation for missing values
   - Train-test split with fixed random seed

2. **Baseline model**
   - Logistic regression with stepwise-selected features
   - Demonstrates failure under severe class imbalance
   - AUC ≈ 0.61 with zero recall

3. **Diagnostics**
   - Examination of confusion matrix, ROC curve, and odds ratios
   - Identification of threshold and imbalance-related failure modes

4. **Feature-driven experiment**
   - Single-feature model using `last_fico_range_high`
   - Achieves AUC ≈ 0.95
   - Demonstrates the impact of strong signal features over feature quantity

---

## Key Insight

Model performance is often constrained by **feature signal quality rather than
model complexity**.  
Targeted feature analysis can outperform complex multivariate models built on
weak signals.

---

## Example Applications

- Credit risk modeling
- Default prediction diagnostics
- Feature selection validation
- Risk analytics under imbalanced outcomes

---

## Tools

- Python
- pandas, numpy
- scikit-learn
- statsmodels
- matplotlib

---

## Notes

This repository contains a refactored academic project presented for
professional and demonstration purposes.  
Data has been anonymized or sampled, and results may vary slightly due to
stochastic imputation.

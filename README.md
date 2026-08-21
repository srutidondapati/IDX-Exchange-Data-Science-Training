# IDX Exchange ML Training
**California Single-Family Home Price Prediction**

A 5-week self-guided machine learning training program for the IDX Exchange 
data science internship. Predicts California residential sale prices using 
CRMLS MLS sold data.

---

## Program Overview

| Week | Focus | Outcome |
|---|---|---|
| Week 1 | Data loading and cleaning | Combined 6 months of MLS data into one clean training table |
| Week 2 | Feature engineering and visualization | Built and justified 11 model features, handled missing values, created exploratory plots |
| Week 3 | Baseline models and evaluation | Trained Linear Regression and Random Forest, reported 5 metrics |
| Week 4 | Model improvement | Applied log-transformation and structural outlier removal |
| Week 5 | XGBoost and final evaluation | Trained final model, evaluated on held-out test set |

---

## Final Model Results (Validation Set)

| Model | R² | MAE | MDAPE |
|---|---|---|---|
| Linear Regression | 0.80 | $211,445 | 15.28% |
| Random Forest | 0.88 | $148,755 | 8.47% |
| XGBoost | 0.89 | $144,614 | 8.88% |

---

## Features Used
- **Location:** Latitude, Longitude, zip_median_price, city_median_price
- **Size:** LivingArea, LotSizeSquareFeet, BedroomsTotal, BathroomsTotalInteger
- **Property traits:** YearBuilt, GarageSpaces, Stories

**Target variable:** ClosePrice

---

## Key Concepts Applied
- Target leakage prevention
- Held-out test set discipline (CRMLSSold202603.csv locked until Week 5)
- ZIP and city median prices computed on training data only
- 5-question feature selection framework
- Log-transformation of skewed price distribution
- Structural outlier removal

---

## Data
CSV files are not included in this repository (proprietary MLS data).
Seven monthly CRMLS sold files were used — six for training 
(Sep 2025 – Feb 2026) and one held out as the final test set (Mar 2026).

---

## Tools
Python, pandas, NumPy, scikit-learn, XGBoost, matplotlib, Google Colab

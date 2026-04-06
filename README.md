# Credit Risk Prediction for ZeitPay GmbH (Fintech)

## Overview
This project develops a predictive model to identify credit default risk for a Berlin-based "Buy Now, Pay Later" startup. 

## Technical Stack
- **Language:** Python 3.x
- **Libraries:** Pandas, Scikit-Learn, Seaborn, Matplotlib
- **Model:** Random Forest Classifier (Accuracy: 98%)

## Key Insights
- **Primary Risk Driver:** Past Defaults & SCHUFA Score.
- **Business Impact:** Identified a "High Risk" segment that accounts for 85% of potential defaults.
- **Recommendation:** Automated rejection for SCHUFA scores below 500.

### Technical Logic & FAQ
**Q: Why use a Random Forest Classifier for this dataset?**
* **A:** Random Forest is excellent for credit scoring because it handles non-linear relationships. For example, a "Medium" SCHUFA score might be "Low Risk" for a high-income earner but "High Risk" for a low-income earner. A simple linear model might miss these nuances.

**Q: What is the significance of the Debt-to-Income (DTI) Ratio?**
* **A:** Raw loan amounts don't tell the whole story. By engineering the DTI feature, the model can see the relative financial "burden" on the borrower, which is a much stronger predictor of default than the loan size alone.

**Q: Is 98% accuracy realistic in a production environment?**
* **A:** While 98% is high, in this controlled simulation it demonstrates that the features (SCHUFA and Past Defaults) have a very strong mathematical correlation with the target. In a real-world scenario, I would further investigate "Data Leakage" to ensure the model isn't seeing the "future" before making a prediction.

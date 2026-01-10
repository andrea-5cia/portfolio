# 🎓 Student Dropout Early Prediction (University of Pavia)

## 🎯 Objective
Develop a **machine learning model** capable of predicting, *at the time of enrollment*, which students are at higher risk of dropping out.  
The goal is to provide an **early warning system** that enables preventive support actions by the University of Pavia.

---

## 🧰 Tech Stack
- **Python:** pandas, scikit-learn, XGBoost, imbalanced-learn, matplotlib  
- **Environment:** Jupyter Notebook (`ml_abb3_early_v4.ipynb`)  
- **Evaluation:** Accuracy, Precision, Recall, F1, ROC-AUC  

---

## 📊 Dataset
- Students enrolled in the **2021–2023 academic years**  
- Variables grouped in 5 dimensions:
  1. Geographic origin (residence, distance, province/city)
  2. School background (type of diploma, grade, honors)
  3. Demographic info (age, gender, citizenship)
  4. Study choice (degree program, department, admission type)
  5. Orientation events participation (COR)

All data were anonymized and derived from internal administrative databases of **Università di Pavia**.

---

## ⚙️ Data Preparation & Feature Engineering
Key preprocessing steps (see *pages 3–6 of the PDF*):
1. **Cleaning & selection** of relevant variables  
   → Removed redundant or textual fields, corrected anomalies in dropout flag.  
2. **Normalization** of categorical variables  
   → Encoded gender, degree type, citizenship, department (One-Hot Encoding).  
3. **Feature creation**
   - *Proximity rank* → distance of residence from campus  
   - *Provincial capital flag* → socio-economic proxy  
   - *School vs residence alignment* → mobility indicator  
4. **Resampling**  
   → Applied **SMOTE** to balance the minority “dropout” class.

Resulting dataset: balanced, compact, and standardized for modeling.

---

## 🤖 Modeling Approach
Multiple algorithms were tested (*page 8*):
| Model | ROC-AUC | Recall | Key traits |
|-------|----------|---------|-------------|
| Decision Tree | 0.56 | – | Baseline |
| Random Forest | 0.62 | – | Moderate improvement |
| Logistic Regression | 0.64 | High recall, interpretable |
| SVM | 0.67 | Balanced but slow |
| **XGBoost (tuned)** | **0.68 AUC / 0.71 accuracy** | Best trade-off |

Final selected models:
- **XGBoost (tuned)** → main predictive engine  
- **Logistic Regression** → complementary, interpretable baseline

---

## 📈 Results
*See pages 10–13 for visuals (confusion matrices, metrics by threshold)*

- **Optimal threshold (F1 ≈ 0.345):**  
  - Recall = 0.68 → captures ~2 out of 3 dropouts  
  - Precision = 0.38  
  - Accuracy ≈ 0.60  
  - AUC = 0.685  

- **Alternative (F2 ≈ 0.215):**  
  - Recall ≈ 0.96 → maximum detection, many false alarms

The tuned XGBoost achieved the best balance between sensitivity and interpretability.  
Logistic Regression remained valuable for communicating variable impact to stakeholders.

---

## 🧠 Explainability
*Pages 14–15* show global and local interpretability analysis:
- **Logistic Regression coefficients:** highlight how higher diploma grades and orientation-event participation reduce dropout probability.  
- **SHAP values (XGBoost):** visualize individual variable contributions (age ↑ risk, event participation ↓ risk, open-admission ↑ risk).

---

## 🧩 Operational Takeaways
1. **Early model (enrollment phase):** enables pre-emptive alerts despite limited data.  
2. **Future extensions:**
   - *Mid model* (November) → include first-semester admin & digital-learning data.  
   - *Post-session model* → integrate exam outcomes for higher precision.  
   - Build a **progressive model ecosystem** improving accuracy through the academic timeline.

---

## 🧾 Files
| File | Description |
|------|--------------|
| [`ml_abb3_early_v4.ipynb`](ml_abb3_early_v4.ipynb) | Full preprocessing, modeling, and evaluation notebook |
| [`Abbandoni-UNIPV-early-predicting.pdf`](Abbandoni-UNIPV-early-predicting.pdf) | Executive presentation with visuals and results summary |

---

## 🗣️ Presentation
The PDF presentation concisely communicates **findings and recommendations** to non-technical stakeholders (University Quality & Demand Management Office).  
💡 Presentation made with Gamma AI

---

## 📬 Author
**Andrea Sciarrillo**  
Data Analyst & Data Scientist

---

## 🏷️ License
MIT License © 2026 Andrea Sciarrillo

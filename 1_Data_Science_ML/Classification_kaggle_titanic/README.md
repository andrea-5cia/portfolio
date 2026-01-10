# 🚢 Titanic Survival Prediction & ChatGPT Model Comparison

## 🎯 Objective
This project revisits my **first machine learning project**, originally developed one year earlier, with the goal of:
- consolidating data science fundamentals,
- improving model design through data-driven feature selection,
- experimentally comparing my approach with a **machine learning model proposed by the first public release of ChatGPT**.

The classic **Kaggle Titanic dataset** is used as a benchmark problem.

---

## 🧰 Tech Stack
- **Python:** pandas, numpy, scikit-learn, matplotlib, seaborn
- **Models:** Support Vector Machine, Decision Tree
- **Environment:** Jupyter Notebook (`kaggle_titanic.ipynb`)

---

## 📊 Dataset
- Source: **Kaggle – Titanic: Machine Learning from Disaster**
- Target variable: `Survived` (binary classification)
- Features include:
  - demographic variables (age, sex),
  - socio-economic indicators (class, fare),
  - family structure (siblings/spouses, parents/children).

The dataset is widely used for educational purposes and public benchmarking.

---

## 🔎 Methodology

### 1. Exploratory Data Analysis
- Statistical inspection of numerical variables
- Analysis of categorical distributions
- Correlation heatmap to identify redundant or weakly informative features
- Visualization of survival patterns by gender, class, and family status

EDA insights were used to **formulate hypotheses** and guide feature selection.

---

### 2. Feature Engineering & Selection
Multiple feature subsets were tested:
- **Full feature set**
- **Reduced sets** based on:
  - correlation analysis,
  - domain reasoning,
  - redundancy removal (e.g. marital status vs. relationship)

This iterative approach allowed a progressive simplification of the model while preserving predictive power.

---

### 3. Machine Learning Models
The following models were implemented and compared:

| Model | Notes |
|------|------|
| Support Vector Machine | High computational cost, baseline reference |
| Decision Tree | Full feature set |
| “Light” Decision Tree | Reduced feature set based on EDA |
| “Skinny” Decision Tree | Minimal feature set, strongest assumptions |
| **ChatGPT Decision Tree** | Model structure and feature selection proposed by ChatGPT |

The ChatGPT-generated model included fewer features and followed a generic ML pipeline.

---

## 🤖 ChatGPT Comparison
The experiment tested ChatGPT’s ability to:
- load and preprocess a dataset,
- encode categorical variables,
- split training and test sets,
- train and evaluate a supervised model.

While ChatGPT successfully generated **working and coherent code**, key limitations emerged:
- basic feature encoding choices,
- lack of domain-driven feature selection,
- lower performance on minority class prediction.

This highlighted the **importance of human reasoning and data understanding**, especially in early-stage ML workflows.

---

## 📈 Results Summary
(See *page 15 of the PDF presentation*)

- Decision Tree models refined through EDA achieved **higher accuracy and better class balance** than baseline models.
- The ChatGPT-generated model performed reasonably well, but:
  - relied on a simplified feature set,
  - showed weaker recall on the positive class.
- The best-performing models were those **explicitly informed by exploratory analysis**.

---

## 🧠 Key Takeaways
- Revisiting an old project is an effective way to **measure technical growth**.
- Data understanding and feature reasoning remain central to ML performance.
- Generative AI tools like ChatGPT are valuable for:
  - rapid prototyping,
  - boilerplate code generation,
but **cannot replace domain-aware modeling decisions**.

This project marks a transition from *learning algorithms* to *thinking like a data scientist*.

---

## 🧾 Files
| File | Description |
|------|-------------|
| [`kaggle_titanic.ipynb`](kaggle_titanic.ipynb) | Full EDA, feature engineering, and model comparison |
| [`Machine-learning-titanic-presentation.pdf`](Machine-learning-titanic-presentation.pdf) | Presentation summarizing analysis, models, and results |

---

## 🗣️ Communication
The PDF presentation documents the analytical reasoning and includes a structured comparison between human-designed models and the ChatGPT-generated solution.

---

## 📬 Author
**Andrea Sciarrillo**  
Data Analyst & Data Scientist  
📧 andreasciarrillo1998@gmail.com | [LinkedIn](https://linkedin.com/in/andrea598)

---

## 🏷️ License
MIT License © 2026 Andrea Sciarrillo

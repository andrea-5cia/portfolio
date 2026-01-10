# 🧠 NLP Analysis of Student Dropout Motivations

## 🎯 Objective
Explore and analyze **free-text dropout requests** submitted by students to identify recurring **motivations and themes behind university withdrawal**.  
The project aims to complement quantitative dropout models with **qualitative insights** derived from natural language data.

---

## 🧰 Tech Stack
- **Python:** pandas, numpy, scikit-learn, nltk, spaCy
- **NLP techniques:** text cleaning, lemmatization, TF–IDF, topic modeling
- **Environment:** Jupyter Notebook (`dl_dmds.ipynb`)

---

## 📊 Dataset
- Source: Administrative records from **Università di Pavia**
- Data type: **Free-text fields** from formal dropout requests
- Language: Italian
- Privacy: All texts were anonymized before analysis

Each record represents a student-submitted motivation for withdrawal, written in natural language.

---

## 🔎 Methodology

### 1. Text Preprocessing
- Lowercasing
- Removal of punctuation, numbers, and stopwords
- Lemmatization (Italian language model)
- Filtering of very short or non-informative texts

### 2. Feature Extraction
- **TF–IDF vectorization** to represent documents numerically
- Vocabulary pruning to remove rare or overly frequent terms

### 3. Exploratory NLP Analysis
- Term frequency analysis
- N-grams inspection
- Identification of dominant keywords and expressions

### 4. Topic Exploration
- Unsupervised exploration of latent themes
- Qualitative interpretation of clusters/topics rather than strict labeling

---

## 📈 Key Findings
The analysis highlights recurring dropout motivations, including:
- **Mismatch between expectations and course content**
- **Academic difficulty and workload**
- **Change of interests or career plans**
- **Logistical and personal constraints** (distance, work, family)
- **Administrative or organizational issues**

Rather than a single dominant cause, dropout emerges as a **multifactorial phenomenon**, often combining academic, personal, and contextual elements.

---

## 🧠 Interpretation
- NLP provides a **valuable qualitative layer** that complements statistical and predictive dropout models.
- Text analysis helps institutions move beyond binary outcomes (dropout / no dropout) toward **understanding “why” students leave**.
- Results are best used for:
  - hypothesis generation,
  - support policy design,
  - qualitative reporting.

---

## 🧾 Files
| File | Description |
|------|-------------|
| [`dl_dmds.ipynb`](dl_dmds.ipynb) | Full NLP preprocessing, analysis, and exploratory modeling |

---

## 🗣️ Communication Note
No standalone presentation was produced for this project.  
The **notebook itself serves as both analytical and explanatory artifact**, making the reasoning process transparent and reproducible.

---

## 📬 Author
**Andrea Sciarrillo**  
Data Analyst & Data Scientist 
📧 andreasciarrillo1998@gmail.com | [LinkedIn](https://linkedin.com/in/andrea598)

---

## 🏷️ License
MIT License © 2026 Andrea Sciarrillo

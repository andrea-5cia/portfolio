# 💬 NLP & Sentiment Analysis on Internship Feedback (2022–2024)

## 🎯 Objective
Apply **Natural Language Processing and Sentiment Analysis** to free-text comments collected through internship evaluation questionnaires, with the goal of:
- identifying recurring themes and perceptions,
- measuring overall sentiment,
- supporting Quality Assurance processes with qualitative insights.

The project analyzes feedback from both **students** and **company tutors** over the **2022–2024** period.

---

## 🧰 Tech Stack
- **Python:** pandas, numpy, scikit-learn
- **NLP:** TF–IDF, Bag-of-Words, n-grams
- **Deep Learning:** XLM-RoBERTa (multilingual transformer)
- **Visualization:** matplotlib, seaborn
- **Environment:** Jupyter Notebook (`nlp_quest_prod.ipynb`)

---

## 📊 Dataset
- Source: **AlmaLaurea internship evaluation questionnaires**
- Provider: Career Orientation Office (COR), University of Pavia
- Period: **2022–2023–2024**
- Data types:
  - Closed-ended questions (Likert scale)
  - **Free-text comments** (students and company tutors)

Only the **open-ended question E4 (student side)** was used for NLP analysis, resulting in **518 cleaned textual records** after preprocessing :contentReference[oaicite:0]{index=0}.

All data were anonymized prior to analysis.

---

## 🔎 Methodology Overview

### 1. Text Cleaning & Preparation
- Removal of missing values and boilerplate phrases (e.g. “no comments”)
- Text length filtering
- Tokenization and **lemmatization (Italian language)**
- Stopword removal (temporarily excluded for frequency analysis)

This step ensures consistency and robustness before modeling.

---

### 2. Exploratory NLP (Bag of Words)
- Unigram and bigram frequency analysis
- Word clouds and ranked term distributions
- Identification of dominant concepts (e.g. *azienda*, *esperienza*, *formativo*)

This phase provides **transparent, interpretable insights** into the vocabulary used by respondents :contentReference[oaicite:1]{index=1}.

---

### 3. Sentiment Analysis (Deep Learning)
- Model: **XLM-RoBERTa**, multilingual transformer
- Approach:
  - Pre-trained on large multilingual corpora
  - Fine-tuned on sentiment-labeled social media texts
- Output:
  - Predicted sentiment: *positive / negative / neutral*
  - **Confidence score** for each prediction

Average confidence scores:
- Positive: **0.83**
- Negative: **0.75**
- Neutral: **0.56**

Approximately **29.3% of comments** fall into a low-confidence zone (score < 0.7), especially within the neutral class, which is inherently ambiguous :contentReference[oaicite:2]{index=2}.

---

## ⚙️ Code Structure & Reusability

The notebook is intentionally structured as a **plug-and-play analytical pipeline**:

1. **Input layer**
   - Reads raw Excel extracts from AlmaLaurea questionnaires
   - Minimal assumptions on file structure (year-based appends supported)

2. **Preprocessing module**
   - Standardized text cleaning
   - Language-specific normalization
   - Reusable functions for future datasets

3. **Analysis layer**
   - Bag-of-Words statistics
   - Sentiment inference with probability outputs

4. **Output layer**
   - Aggregated sentiment distributions
   - Confidence diagnostics
   - Ready-to-visualize summary tables

➡️ When new Excel files become available, the analysis can be **re-run without structural changes**, making the notebook suitable for **periodic institutional monitoring**.

---

## 📈 Key Findings
- Internship feedback is **overwhelmingly positive**, consistent with quantitative questionnaire results.
- Sentiment analysis confirms high satisfaction levels among both students and companies.
- Negative or critical comments are:
  - relatively rare,
  - highly informative for targeted qualitative follow-ups.
- Neutral sentiment often corresponds to generic or descriptive comments rather than true neutrality.

---

## 🧠 Interpretation & Use
- The project demonstrates how **NLP can complement traditional QA indicators**.
- Particularly useful for:
  - detecting weak signals not captured by Likert-scale questions,
  - guiding qualitative deep dives,
  - enriching reports for QA bodies (e.g. CPDS, Internship Working Groups).

The confidence score analysis helps distinguish **robust insights from uncertain classifications**, improving interpretability.

---

## 🧾 Files
| File | Description |
|------|-------------|
| [`nlp_quest_prod.ipynb`](nlp_quest_prod.ipynb) | End-to-end NLP and sentiment analysis pipeline |
| [`Report analisi questionari tirocinio.pdf`](Report%20analisi%20questionari%20tirocinio.pdf) | Executive report with statistics, NLP results, and visualizations |

---

## 🗣️ Communication
The PDF report translates technical findings into **decision-ready insights** for Quality Assurance stakeholders and institutional bodies :contentReference[oaicite:3]{index=3}.

---

## 📬 Author
**Andrea Sciarrillo**  
Data Analyst & Data Scientist
📧 andreasciarrillo1998@gmail.com | [LinkedIn](https://linkedin.com/in/andrea598)

---

## 🏷️ License
MIT License © 2026 Andrea Sciarrillo

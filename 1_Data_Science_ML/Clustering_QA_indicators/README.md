# 🎓 Clustering PhD Programs Using Quality Assurance Indicators (AVA3)

## 🎯 Objective
Apply **unsupervised learning techniques** to identify structural patterns among PhD programs based on official **AVA3 Quality Assurance indicators**.  
The goal is to support **exploratory benchmarking** and provide a synthetic, data-driven overview of program profiles for institutional evaluation purposes.

---

## 🧰 Tech Stack
- **Python:** pandas, numpy, scikit-learn, matplotlib, seaborn
- **Methods:** K-means clustering, PCA
- **Environment:** Jupyter Notebook (`latest_ind_phd_v3.ipynb`)

---

## 📊 Dataset
- Source: Internal QA datasets – **Università di Pavia**
- Scope: **PhD programs**, years **2020–2024**
- Unit of analysis: *PhD program × indicator*
- Only **robust indicators** were included (denominator ≥ 10, “green flag”)

### AVA3 Indicators used
- **H.0.0.A** – % first-year PhD students with a degree from another university  
- **H.0.0.B** – % PhD graduates with ≥3 months abroad  
- **H.0.0.C** – % PhD scholarships funded by external institutions  
- **H.0.0.D** – % PhD graduates with ≥6 months in other institutions  
- **H.0.0.E** – Research products per PhD graduate (last 3 cycles)

Each record includes indicator values, national/regional benchmarks, and robustness flags.

---

## ⚠️ Data Limitations
As discussed in the PDF (pp. 2–3):
- **Small sample sizes** for many programs → high statistical instability  
- **Heterogeneous data completeness** across programs  
- Extreme values amplified by small denominators  

➡️ Results must be interpreted as **exploratory**, not prescriptive.

---

## 🔎 Methodology

### 1. Data Aggregation
- Computed **average indicator values (2020–2024)** per PhD program  
- Built a **program × indicator matrix**
- Retained only indicators with robust denominators

### 2. Clustering
- Algorithm: **K-means**
- Number of clusters: **k = 4**
- Selection criteria:
  - Elbow method (inertia)
  - Silhouette analysis

**Silhouette score:** `0.38`  
→ moderate separation: clusters are interpretable but partially overlapping.

### 3. Dimensionality Reduction
- **PCA (2 components)** used for visualization and qualitative validation of cluster separation.

---

## 📈 Results

### Identified Clusters (k = 4)
Based on indicator profiles (see PDF pp. 12–13):

| Cluster | Profile |
|--------|--------|
| **Cluster 0** | High **external attractiveness** (H.0.0.A) and strong **external funding** (H.0.0.C) |
| **Cluster 1** | Overall **medium–low indicators**, no specific strengths |
| **Cluster 2** | High **scientific productivity** (H.0.0.E) |
| **Cluster 3** | Strong **internationalization** (H.0.0.B, H.0.0.D) |

Clusters 0 and 1 include the majority of PhD programs, while clusters 2 and 3 represent more **specialized profiles**.

---

## 🧠 Interpretation & Use
- The clustering provides a **synthetic segmentation** of PhD programs based on QA dimensions.
- Useful for:
  - exploratory benchmarking,
  - identifying *structural similarities*,
  - supporting qualitative evaluation by QA bodies.

⚠️ Due to data robustness issues and moderate silhouette score, results should **not** be used for ranking or performance evaluation.

---

## 🧾 Files
| File | Description |
|------|-------------|
| [`latest_ind_phd_v3.ipynb`](latest_ind_phd_v3.ipynb) | Full data preparation, clustering, and PCA analysis |
| [`Clustering_Analisi Indicatori AVA3-PhD_v2.pdf`](Clustering_Analisi%20Indicatori%20AVA3-PhD_v2.pdf) | Executive presentation with trends, benchmarking, and cluster interpretation |

---

## 🗣️ Communication
The PDF presentation was designed for **non-technical stakeholders** (Quality Assurance Office, Evaluation Board) and complements the notebook by translating analytical results into institutional insights.

---

## 📬 Author
**Andrea Sciarrillo**  
Data Analyst & Data Scientist  
📧 andreasciarrillo1998@gmail.com | [LinkedIn](https://linkedin.com/in/andrea598)

---

## 🏷️ License
MIT License © 2026 Andrea Sciarrillo

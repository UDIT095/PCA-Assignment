# 🧪 Dimensionality Reduction with PCA and Clustering Analysis on Wine Data

## 📌 Project Title
**Dimensionality Reduction with PCA and Clustering Analysis on Wine Data**

## 🎯 Objective
This project aims to apply **Principal Component Analysis (PCA)** for dimensionality reduction followed by **K-Means clustering**. It investigates the effect of PCA on clustering performance and explores the trade-offs of dimensionality reduction in unsupervised learning tasks.

---

## 📊 Dataset
- **Source**: `wine.csv`
- **Description**: Contains the results of chemical analysis of wines grown in the same region in Italy but derived from **three different cultivars**.
- **Target**: `Type` (1, 2, or 3 — used for cluster evaluation only)
- **Features**: 13 numerical variables such as Alcohol, Ash, Flavanoids, Color Intensity, etc.

---

## 🧾 Files in this Repository
| File Name      | Description                                                        |
|----------------|--------------------------------------------------------------------|
| `wine.csv`     | The dataset used for PCA and clustering                            |
| `PCA.docx`     | Assignment objectives and instructions                             |
| `PCA.ipynb`    | Jupyter notebook with full EDA, PCA, clustering, and evaluation code |

---

## 🛠️ Tools and Libraries Used
- **pandas** – Data loading and manipulation  
- **matplotlib**, **seaborn** – Data visualization  
- **scikit-learn**:
  - `StandardScaler` – Feature scaling  
  - `PCA` – Dimensionality reduction  
  - `KMeans` – Clustering  
  - `silhouette_score`, `davies_bouldin_score` – Evaluation metrics  

---

## 🔍 Project Workflow

### ✅ Task 1: Exploratory Data Analysis (EDA)
- Loaded and explored the dataset (`df.head()`, `df.describe()`, `df.info()`)
- Visualized feature distributions and correlations using heatmaps

### ✅ Task 2: PCA for Dimensionality Reduction
- Standardized the data
- Applied PCA to identify the minimum number of components capturing significant variance
- Determined that **2 principal components** explain ~55% variance

### ✅ Task 3: Clustering on Original Data
- Applied **K-Means** on scaled original data (k=3)
- Visualized clusters in 2D (via PCA-reduced space)
- Evaluated using:
  - **Silhouette Score**
  - **Davies-Bouldin Index**

### ✅ Task 4: Clustering on PCA Data
- Performed K-Means on 2D PCA-transformed data
- Visualized clustering result
- Compared performance with clustering on original features

### ✅ Task 5: Comparison & Insights
- **PCA-transformed data showed slightly improved clustering performance**
  - Higher Silhouette Score
  - Lower Davies-Bouldin Index
- PCA reduced correlated noise and helped improve clustering separability

---

## 📈 Results Summary

| Dataset        | Silhouette Score | Davies-Bouldin Index |
|----------------|------------------|-----------------------|
| Original       | 0.28             | 0.68                  |
| PCA (2D)       | 0.30             | 0.61                  |

- **Conclusion**: PCA helped simplify the dataset and marginally improved clustering, confirming its utility in high-dimensional unsupervised learning tasks.

---

## 🧠 Key Learnings
- PCA is an effective pre-processing step for clustering when dealing with correlated or high-dimensional data.
- Although dimensionality reduction may lead to information loss, it can also enhance clustering clarity and reduce computational load.

---

## ▶️ How to Run the Notebook

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```

2. **Install Required Libraries**
   ```bash
   pip install pandas matplotlib seaborn scikit-learn
   ```

3. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

4. **Run `PCA.ipynb`**
   - Execute all cells in order to reproduce the full workflow: EDA → PCA → Clustering → Evaluation.

---

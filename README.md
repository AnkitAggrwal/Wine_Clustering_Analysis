# 🍷 Clustering Analysis on UCI Wine Dataset

This project presents a comparative performance study of different clustering algorithms using various preprocessing techniques and evaluation metrics. The UCI Wine dataset was used for unsupervised learning and cluster quality evaluation.

---

## 📁 Dataset
- **Source**: [UCI Machine Learning Repository - Wine Dataset](https://archive.ics.uci.edu/ml/datasets/wine)
- **Samples**: 178
- **Features**: 13 chemical attributes of wines from 3 cultivars

---

## 🔍 Objective
To evaluate and compare the effectiveness of different clustering algorithms on differently preprocessed versions of the dataset using metrics like:
- Silhouette Score
- Calinski-Harabasz Index
- Davies-Bouldin Index

---

## ⚙️ Preprocessing Techniques

1. **RAW** – Original data (no preprocessing)
2. **StandardScaler** – Standardized features
3. **MinMaxScaler** – Normalized features between 0 and 1
4. **StandardScaler + PCA (2D)** – Dimensionality reduced data for 2D visualization

---

## 🤖 Clustering Algorithms

- **KMeans** (k = 3)
- **Agglomerative Clustering** (k = 3)
- **MeanShift** (automatic number of clusters)

---

## 📊 Evaluation Metrics

| Metric               | Description |
|----------------------|-------------|
| Silhouette Score     | Measures cohesion and separation (higher is better) |
| Calinski-Harabasz    | Measures between-cluster dispersion (higher is better) |
| Davies-Bouldin Index | Lower is better; measures intra-cluster similarity |

---

## 📈 Results Summary

| Preprocessing | Method            | Silhouette Score | Calinski-Harabasz | Davies-Bouldin |
|---------------|-------------------|------------------|-------------------|----------------|
| STD           | KMeans (k=3)      | *0.xx*           | *xxx.x*           | *x.xx*         |
| NORM          | KMeans (k=3)      | *0.xx*           | *xxx.x*           | *x.xx*         |
| PCA           | KMeans (k=3)      | *0.xx*           | *xxx.x*           | *x.xx*         |
| STD           | Agglomerative     | *0.xx*           | *xxx.x*           | *x.xx*         |
| ...           | ...               | ...              | ...               | ...            |

📌 *Note: Some MeanShift runs resulted in only one cluster and were excluded from evaluation metrics.*

---

## 📉 Visualizations

- 📌 **PCA 2D Scatter Plots** of clustering for visual comparison
- 📊 **Bar charts** comparing evaluation scores across methods and preprocessing techniques

<p align="center">
  <img src="results/cluster_plots.png" width="600" />
</p>

<p align="center">
  <img src="results/evaluation_table.png" width="600" />
</p>

---

## 🧠 Conclusion

- **StandardScaler + KMeans** showed consistently strong performance.
- **PCA** helped visualize cluster separation clearly in 2D, but occasionally reduced performance due to information loss.
- **MeanShift** was not suitable for this dataset as it frequently found only one cluster.

---

## 📂 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/AnkitAggrwal/wine-clustering-analysis.git

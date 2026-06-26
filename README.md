# 📊 Industry-Level Clustering Algorithm Comparison Benchmark

An end-to-end **Unsupervised Machine Learning** project that benchmarks three of the most widely used clustering algorithms:

- 🔵 K-Means Clustering
- 🟣 Agglomerative Hierarchical Clustering
- 🔴 DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

The project generates a realistic synthetic **Customer Segmentation** dataset containing clusters of varying densities along with random noise (outliers), then evaluates how each algorithm performs using industry-standard clustering metrics and visualizations.

---

# 📌 Project Overview

Customer segmentation is one of the most common applications of unsupervised machine learning. Different clustering algorithms perform differently depending on:

- Cluster shape
- Cluster density
- Presence of outliers
- Dataset size
- Computational complexity

This project demonstrates these differences by comparing K-Means, Hierarchical Clustering, and DBSCAN on the same dataset using quantitative evaluation metrics and graphical analysis.

---

# 🚀 Features

## 📊 Synthetic Dataset Generation

A realistic customer dataset is generated using **Scikit-Learn's `make_blobs()`** with:

- 4 customer clusters
- Different cluster densities
- 1,500 clustered samples
- 100 uniformly distributed noise points (outliers)

This creates a challenging dataset suitable for evaluating clustering algorithms.

---

## ⚙️ Data Preprocessing

Before clustering:

- Standardizes features using **StandardScaler**
- Performs **Principal Component Analysis (PCA)** for 2D visualization

Since all three algorithms are distance-based, feature scaling is essential.

---

## 📈 K-Means Hyperparameter Analysis

The notebook evaluates multiple values of **K** using:

- Elbow Method (Inertia)
- Silhouette Score

The comparison helps determine the optimal number of clusters before fitting the final K-Means model.

---

## 🌳 Hierarchical Clustering Analysis

Agglomerative Clustering is analyzed through:

- Ward Linkage
- Euclidean Distance
- Dendrogram Visualization

The dendrogram illustrates the hierarchical relationship between customer groups before selecting the cluster cut.

---

## 🔍 DBSCAN Parameter Selection

To estimate an appropriate **Epsilon (ε)** value, the notebook generates a:

- K-Distance Graph
- 5-Nearest Neighbor Distance Plot

DBSCAN is then fitted using:

- `eps = 0.25`
- `min_samples = 5`

allowing it to identify noise points automatically.

---

## 📊 Algorithm Visualization

Each clustering algorithm is visualized after PCA dimensionality reduction:

- K-Means Clusters
- Hierarchical Clusters
- DBSCAN Clusters

Noise points detected by DBSCAN are highlighted in **red**.

---

## 📉 Performance Benchmark

Each algorithm is evaluated using industry-standard clustering metrics:

- Silhouette Score
- Calinski-Harabasz Index
- Davies-Bouldin Index
- Execution Latency (milliseconds)

The results are displayed both as:

- Comparison Table
- Graphical Dashboard

---

# 🧠 Algorithms Compared

## 🔵 K-Means

### Type
Centroid-Based Clustering

### Advantages

- Fast execution
- Highly scalable
- Easy to interpret
- Excellent for spherical clusters

### Limitations

- Sensitive to outliers
- Requires predefined K
- Assumes similar cluster sizes

---

## 🟣 Agglomerative Hierarchical

### Type

Connectivity-Based Clustering

### Advantages

- Produces hierarchical relationships
- Dendrogram visualization
- No centroid assumptions

### Limitations

- Computationally expensive
- Less scalable for very large datasets

---

## 🔴 DBSCAN

### Type

Density-Based Clustering

### Advantages

- Detects arbitrary-shaped clusters
- Automatically identifies outliers
- Does not require specifying the number of clusters

### Limitations

- Sensitive to ε (Epsilon)
- Sensitive to MinPts
- Performance depends on parameter selection

---

# 📈 Evaluation Metrics

| Metric | Description | Best Value |
|----------|-------------|------------|
| Silhouette Score | Measures cluster cohesion and separation | Higher ↑ |
| Calinski-Harabasz Index | Ratio of between-cluster to within-cluster variance | Higher ↑ |
| Davies-Bouldin Index | Measures similarity between clusters | Lower ↓ |
| Execution Latency | Time required for clustering | Lower ↓ |

---

# 🛠️ Technologies Used

## Programming Language

- Python 3.8+

## Libraries

- NumPy
- Pandas
- Scikit-Learn
- SciPy
- Matplotlib
- Seaborn

---

# 📦 Installation

Clone the repository

```bash
git clone https://github.com/your-username/Industry-Level-Clustering-Benchmark.git
```

Move into the project folder

```bash
cd Industry-Level-Clustering-Benchmark
```

Install dependencies

```bash
pip install numpy pandas scikit-learn scipy matplotlib seaborn
```

---

# ▶️ Project Workflow

```text
Generate Customer Dataset
          │
          ▼
Feature Standardization
(StandardScaler)
          │
          ▼
Dimensionality Reduction
(PCA)
          │
          ▼
──────────────────────────────────
│          K-Means               │
│  • Elbow Method                │
│  • Silhouette Analysis         │
──────────────────────────────────
          │
          ▼
──────────────────────────────────
│      Hierarchical              │
│  • Ward Linkage                │
│  • Dendrogram                  │
──────────────────────────────────
          │
          ▼
──────────────────────────────────
│          DBSCAN                │
│  • K-Distance Graph            │
│  • Noise Detection             │
──────────────────────────────────
          │
          ▼
Performance Evaluation
          │
          ▼
Comparison Dashboard
```
---
# 📷 Results & Visualizations

## 📊 Raw Customer Dataset

The synthetic dataset consists of four customer segments with different densities along with randomly generated outliers.



---

## 📈 K-Means Hyperparameter Analysis

The Elbow Method and Silhouette Score are used to determine the optimal number of clusters.



---

## 🌳 Hierarchical Clustering Dendrogram

Ward linkage is used to visualize hierarchical relationships between customer groups.



---

## 🔍 DBSCAN Parameter Selection

The K-Distance Graph helps estimate the optimal ε (epsilon) value.



---

## 🎯 Clustering Results Comparison

The following figure compares the clustering performance after PCA dimensionality reduction.

- **K-Means**
- **Hierarchical Clustering**
- **DBSCAN**

Noise points detected by DBSCAN are shown in **red**.



---

## 📋 Performance Comparison Matrix

The notebook compares all algorithms using multiple clustering evaluation metrics.



---

## 📊 Performance Dashboard

The evaluation dashboard compares:

- Silhouette Score
- Calinski-Harabasz Index
- Davies-Bouldin Index
- Computational Latency



---
---

# 📂 Outputs

The notebook generates:

- ✅ Raw Customer Dataset Visualization
- ✅ Elbow Method Plot
- ✅ Silhouette Score Plot
- ✅ Hierarchical Dendrogram
- ✅ K-Distance Graph
- ✅ PCA Visualization of K-Means
- ✅ PCA Visualization of Hierarchical Clustering
- ✅ PCA Visualization of DBSCAN
- ✅ Performance Comparison Table
- ✅ Performance Comparison Dashboard

---

# 💡 Key Insights

### 🔹 K-Means

- Fastest algorithm
- Performs well on compact spherical clusters
- Sensitive to outliers

---

### 🔹 Hierarchical Clustering

- Provides interpretable hierarchical structures
- Produces dendrograms
- Higher computational cost

---

### 🔹 DBSCAN

- Successfully identifies noise points
- Handles irregular cluster shapes
- Performance depends on proper parameter tuning

---

# 📊 Performance Comparison

The notebook compares algorithms using:

- Silhouette Score
- Calinski-Harabasz Index
- Davies-Bouldin Index
- Computational Latency

making it easy to evaluate clustering quality from both analytical and business perspectives.

---

# 🎯 Learning Outcomes

This project demonstrates:

- Synthetic data generation
- Data preprocessing
- Feature scaling
- PCA visualization
- K-Means clustering
- Hierarchical clustering
- DBSCAN clustering
- Hyperparameter analysis
- Clustering evaluation metrics
- Comparative performance benchmarking
- Data visualization using Matplotlib and Seaborn

---

# ⭐ If you found this project useful, consider giving it a star!

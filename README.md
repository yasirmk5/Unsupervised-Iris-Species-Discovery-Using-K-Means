# Unsupervised-Iris-Species-Discovery-Using-K-Means
<img width="1024" height="367" alt="image" src="https://github.com/user-attachments/assets/e1f4a1d8-2621-49c0-aa28-5a4741a83e4b" />
Iris Dataset — PCA & K-Means Clustering
 Project Overview

This project demonstrates dimensionality reduction and unsupervised machine learning using the famous Iris dataset.

The dataset is first standardized, then reduced from 4 dimensions to 2 dimensions using Principal Component Analysis (PCA). Finally, K-Means clustering is applied to group the Iris samples into 3 clusters.

 Technologies Used
Python
Scikit-learn
NumPy
Matplotlib
Jupyter Notebook
Dataset

The Iris dataset contains 150 samples with four features:

Sepal Length
Sepal Width
Petal Length
Petal Width

It contains three Iris species:

Setosa
Versicolor
Virginica
 Project Workflow
Iris Dataset
     ↓
Feature Selection
     ↓
StandardScaler
     ↓
PCA (4D → 2D)
     ↓
K-Means Clustering
     ↓
3 Clusters
     ↓
Visualization
 PCA

PCA is used to reduce the dimensionality of the dataset while retaining the most important information.

pca = PCA(n_components=2)
X_pca = pca.fit_transform(X_scaled)

The resulting dataset has the shape:

(150, 2)
 K-Means Clustering

K-Means is used to divide the PCA-transformed data into 3 clusters.

kmeans = KMeans(
    n_clusters=3,
    random_state=42,
    n_init=10
)

labels = kmeans.fit_predict(X_pca)
centers = kmeans.cluster_centers_
 Visualization

The final visualization displays:

Colored points representing the three clusters
Red X markers representing cluster centroids
The first two principal components on the axes
 Note

K-Means cluster labels (0, 1, 2) do not inherently correspond to the Iris species labels. The cluster numbers are assigned by the algorithm and may have a different ordering.

 How to Run
Clone this repository:
git clone <your-repository-url>
Install the required libraries:
pip install numpy pandas matplotlib scikit-learn jupyter
Open the notebook:
jupyter notebook
Run Iris Datasets.ipynb cell by cell.
 Project Structure
Iris-Datasets/
│
├── Iris Datasets.ipynb
└── README.md
 Objective

The main objective of this project is to understand:

Data preprocessing
Feature standardization
Principal Component Analysis (PCA)
K-Means clustering
Cluster visualization
Unsupervised machine learning

Author: Yasirmk

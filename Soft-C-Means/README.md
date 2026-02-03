# 📌 Soft C-Means (Fuzzy C-Means) Clustering — From Scratch

### Machine Learning Algorithms — Custom Implementation in Python
This project is part of the Machine-Learning-Algorithms repository and provides a complete from-scratch implementation of the Soft C-Means (Fuzzy C-Means) algorithm using Python and NumPy.
All computations — including membership updates, centroid updates, and convergence checks — are written manually without ML libraries.
The project also includes clustering visualizations, evaluation metrics, and iterative tracking of the objective function.


## 🚀 Project Highlights
- 🔢 Implements Soft (Fuzzy) C-Means from scratch
- 🎛 Fully parameterized (clusters k, fuzziness m, max iterations, tolerance, etc.)
- 📉 Tracks Jm objective function across iterations
- 🎨 Plots cluster formation, first and last iteration centroids
- 📊 Includes Elbow method and Silhouette coefficient for cluster quality evaluation
- 🧪 Implemented in a clear Jupyter Notebook, ideal for learning or demonstration

## 🧠 What is Soft C-Means?
Soft C-Means (also known as Fuzzy C-Means) is a clustering algorithm where each data point belongs to every cluster with a certain membership degree, rather than being assigned to only one cluster (as in K-Means).
This is especially useful when cluster boundaries are ambiguous.
The goal is to minimize the objective function:  
<p align="center">
$J_m = \sum_{i=1}^{N} \sum_{j=1}^{k} (w_{ij})^m \cdot ||x_i - c_j||$.
</p>

## ⚙️ Algorithm Steps
1. Initialize membership matrix randomly (W), normalized per point.
2. Compute centroids using fuzzy weights.
3. Update membership coefficients using relative distance ratios.
4. Check convergence:  
If $|W_new − W| < ε$, stop.
5. Record objective value Jm at every iteration.
6. Visualize results — cluster assignments, centroids, and convergence curve.

## 🛠 Technologies Used
- Python 3.8+
- NumPy
- Matplotlib
- Scikit-learn (for Silhouette evaluation)

## 📷 Visual Results
### 👉 Elbow Method
Used to determine an optimal number of clusters by comparing distortion values.
images/Elbow\ method.png

### 👉 Silhouette Plot
Visualizes cohesion & separation between clusters.
images/silhouette\ plot.png

### 👉 Jm Objective Function Across Iterations
Used to analyze the convergence of Soft C-Means.
images/Jm\ Change\ through\ Iterations.png

### 👉 Final Clustering Results
Displays the final centroids and cluster assignments.
images/Clusters.png

### 👉 First Iteration (Initial Centroids)
images/First\ iteration.png

### 👉 Last Iteration (Converged Centroids)
images/Last\ iteration.png

## 🧪 Parameters You Can Adjust
```
k = 4        # number of clusters
m = 2        # fuzziness coefficient (>1)
n = 50       # number of samples
d = 2        # number of dimensions
e = 1e-4     # tolerance for convergence
max_iter = 300
```

## ▶️ How to Run
Clone the repo:
```
git clone https://github.com/drga9808/Machine-Learning-Algorithms.git
cd Machine-Learning-Algorithms
```
Install dependencies:
```
pip install numpy matplotlib scikit-learn
```
Open the notebook:
```
jupyter notebook soft_cmeans.ipynb
```
Run all cells to reproduce clustering and visualizations.

## 📊 Evaluation Methods Included
### 1. Elbow Method
Evaluates distortion to suggest an optimal number of clusters.

### 2. Silhouette Score
Measures how similar each point is to its own cluster compared to others.

### 3. Jm Objective Function Tracking
Ensures algorithm converges properly.

## 🔍 Observations from Results
- Jm curve stabilizes → algorithm converged successfully
- Silhouette plot indicates cluster separation quality
- Final centroids visually align with underlying data clusters
- Elbow method shows diminishing returns around k=4

## 📌 Potential Improvements
- Add support for real-world datasets
- Vectorize loops for faster computation
- Add noise-handling or outlier detection
- Convert implementation into a reusable module/class
- Add animation of centroid movement across iterations

## 📄 License
MIT License
Feel free to use, modify, and reference this work with attribution.

## 👤 Author
Daniel Garcia
Developer & Machine Learning Enthusiast
GitHub: https://github.com/drga9808

# README_01_PrincipalComponentAnalysis

## 📌 Syllabus Coverage
This README covers the following from **Session 4 (Linear Algebra Applications – PCA & SVD)**:
- Principal Component Analysis (PCA)
- Dimensionality Reduction
- Eigenvalues and Eigenvectors
- Explained Variance

---

## 1. Definition
**Principal Component Analysis (PCA)** is an unsupervised machine learning algorithm and statistical technique for **dimensionality reduction**.  

- It projects high-dimensional data into a lower-dimensional space.  
- The new dimensions are called **Principal Components (PCs)**.  
- Each PC is a **linear combination of original features**, capturing the maximum variance.  

---

## 2. Why PCA?
- High-dimensional data often has redundant or correlated features.  
- PCA helps to:  
  - Reduce number of variables (dimensionality).  
  - Preserve most of the information (variance).  
  - Remove correlations between features.  

---

## 3. Mathematical Formulation
Given dataset $X$ (standardized):  

1. Compute the **covariance matrix**:  

$$
C = \frac{1}{n-1} X^T X
$$

2. Compute **eigenvalues** and **eigenvectors** of $C$:  

$$
C v = \lambda v
$$

- Eigenvectors = directions of maximum variance (principal components).  
- Eigenvalues = amount of variance captured by each eigenvector.  

3. Sort eigenvectors by descending eigenvalues.  
4. Select top $k$ eigenvectors to form reduced feature space.  

---

## 4. Explained Variance
- Eigenvalues represent the variance explained by each PC.  
- The proportion of variance explained (PVE):  

$$
\text{PVE}_i = \frac{\lambda_i}{\sum_{j=1}^m \lambda_j}
$$

Example:  
- PC1 explains 85.5% of variance.  
- PC2 explains 14.5% of variance.  

Together, PC1 + PC2 ≈ 100% → sufficient to represent original data in 2D.  

---

## 5. Coding Hint (Python)
    import numpy as np
    from sklearn.decomposition import PCA

    # Example data (6 samples, 4 features)
    X = np.array([[11, 6, 12, 5],
                  [10, 4, 9, 7],
                  [8, 5, 10, 6],
                  [3, 3, 2, 2],
                  [2, 3, 1, 4],
                  [1, 2, 2, 7]])

    # Standardize (optional but recommended)
    X = (X - np.mean(X, axis=0)) / np.std(X, axis=0)

    # Apply PCA
    pca = PCA(n_components=2)
    X_pca = pca.fit_transform(X)

    print("Explained variance ratio:", pca.explained_variance_ratio_)
    print("Reduced data:\n", X_pca)

---

## 6. Do It Yourself 🚀
1. Compute the covariance matrix for a $3 \times 3$ dataset and find its eigenvalues and eigenvectors.  
2. Apply PCA in Python to reduce a dataset with 5 features to 2 principal components.  
3. Plot the explained variance ratio to decide how many PCs to keep.  

---

## 7. Memory Tips 🧠
- PCA = “rotate axes to capture maximum variance.”  
- Eigenvector → new axis (direction).  
- Eigenvalue → importance (variance explained).  
- Keep PCs with largest eigenvalues.  

---

✅ By the end of this section, you should understand:
- What PCA is and why it is used  
- How PCA works mathematically  
- The role of eigenvalues and eigenvectors  
- How to apply PCA in Python and interpret explained variance  

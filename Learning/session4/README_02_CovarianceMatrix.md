# README_02_CovarianceMatrix

## 📌 Syllabus Coverage
This README covers the following from **Session 4 (Linear Algebra Applications – PCA & SVD)**:
- Covariance
- Variance vs Covariance
- Covariance Matrix
- Eigen Decomposition of Covariance Matrix

---

## 1. Variance and Covariance
- **Variance** measures how much a single feature varies around its mean.  

$$
\text{Var}(X) = \frac{1}{n-1}\sum_{i=1}^n (x_i - \bar{x})^2
$$  

- **Covariance** measures how two features vary together.  

$$
\text{Cov}(X, Y) = \frac{1}{n-1}\sum_{i=1}^n (x_i - \bar{x})(y_i - \bar{y})
$$  

  - Positive → features increase together.  
  - Negative → one increases while the other decreases.  
  - Zero → no linear relationship.  

---

## 2. Covariance Matrix
For dataset $X$ with $m$ features:  

$$
C = \frac{1}{n-1} X^T X
$$

where $C$ is an $m \times m$ symmetric matrix.  

Example for two features:  

$$
C = \begin{bmatrix}
\text{Var}(X_1) & \text{Cov}(X_1, X_2) \\
\text{Cov}(X_2, X_1) & \text{Var}(X_2)
\end{bmatrix}
$$

---

## 3. Role in PCA
- PCA computes the covariance matrix of standardized data.  
- Then finds its **eigenvalues** and **eigenvectors**.  
  - Eigenvectors → directions of principal components.  
  - Eigenvalues → variance explained by each PC.  

---

## 4. Example
Dataset (features $F1, F2$):  

$$
X = \begin{bmatrix}
12 & 7 \\
10 & 4 \\
2 & 3 \\
8 & 5 \\
3 & 3 \\
1 & 2
\end{bmatrix}
$$

Step 1: Center the data (subtract mean).  
Step 2: Compute covariance matrix $C$.  
Step 3: Find eigenvalues and eigenvectors of $C$.  

---

## 5. Coding Hint (Python)
    import numpy as np

    # Example dataset (6 samples, 2 features)
    X = np.array([[12, 7],
                  [10, 4],
                  [2, 3],
                  [8, 5],
                  [3, 3],
                  [1, 2]])

    # Step 1: Center data
    X_centered = X - np.mean(X, axis=0)

    # Step 2: Covariance matrix
    C = np.cov(X_centered.T)
    print("Covariance Matrix:\n", C)

    # Step 3: Eigen decomposition
    eigvals, eigvecs = np.linalg.eig(C)
    print("Eigenvalues:", eigvals)
    print("Eigenvectors:\n", eigvecs)

---

## 6. Do It Yourself 🚀
1. Compute the covariance matrix for dataset  

   $$
   X = \begin{bmatrix}
   4 & 2 \\
   3 & 5 \\
   6 & 7
   \end{bmatrix}
   $$  

   and find eigenvalues/eigenvectors.  

2. In Python, generate a $5 \times 3$ random dataset and compute its covariance matrix.  

3. Verify symmetry: $C = C^T$.  

---

## 7. Memory Tips 🧠
- Variance = spread of one feature.  
- Covariance = relationship between two features.  
- Covariance matrix = “all pairwise relationships.”  
- Eigenvectors of covariance matrix = principal components.  

---

✅ By the end of this section, you should understand:
- What variance and covariance mean  
- How to construct a covariance matrix  
- How PCA uses eigen decomposition of covariance matrix  
- How to compute covariance matrices in Python  

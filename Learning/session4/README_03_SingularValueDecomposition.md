# README_03_SingularValueDecomposition

## 📌 Syllabus Coverage
This README covers the following from **Session 4 (Linear Algebra Applications – PCA & SVD)**:
- Singular Value Decomposition (SVD)
- Matrix Factorization
- Mathematical formulation
- Steps of computation
- Applications

---

## 1. Definition
**Singular Value Decomposition (SVD)** is a matrix factorization technique that expresses any $m \times n$ matrix $A$ as the product of three matrices:

$$
A = U \Sigma V^T
$$

Where:
- $U$ is an $m \times m$ orthogonal matrix (left singular vectors).  
- $\Sigma$ is an $m \times n$ diagonal matrix (singular values).  
- $V$ is an $n \times n$ orthogonal matrix (right singular vectors).  

---

## 2. Properties
- Columns of $U$ are eigenvectors of $AA^T$.  
- Columns of $V$ are eigenvectors of $A^T A$.  
- Diagonal entries of $\Sigma$ are square roots of eigenvalues of $AA^T$ or $A^T A$.  
- Singular values are sorted in descending order.  

---

## 3. Steps to Compute SVD
1. Start with matrix $A$ (size $m \times n$).  
2. Compute $AA^T$ and $A^T A$.  
3. Find eigenvalues and eigenvectors:  
   - $U$: eigenvectors of $AA^T$  
   - $V$: eigenvectors of $A^T A$  
4. Form $\Sigma$ with square roots of eigenvalues (sorted).  
5. Construct $A = U \Sigma V^T$.  

---

## 4. Example
Let  

$$
A = \begin{bmatrix}
3 & 1 \\
1 & 3
\end{bmatrix}
$$

- Compute $A^T A$ and $AA^T$.  
- Eigenvalues → $\lambda_1, \lambda_2$.  
- Singular values = $\sqrt{\lambda_1}, \sqrt{\lambda_2}$.  
- Build $U, \Sigma, V$.  

---

## 5. Applications of SVD
- **Dimensionality reduction** (similar to PCA).  
- **Noise reduction / denoising** in images.  
- **Image compression** (store fewer singular values).  
- **Recommendation systems** (matrix factorization).  
- **Latent Semantic Analysis (LSA)** in NLP.  

---

## 6. Coding Hint (Python)
    import numpy as np

    # Example matrix
    A = np.array([[3, 1],
                  [1, 3]])

    # Compute SVD
    U, S, Vt = np.linalg.svd(A)

    print("U:\n", U)
    print("Singular values:", S)
    print("V^T:\n", Vt)

    # Reconstruct A
    Sigma = np.zeros((2,2))
    Sigma[:len(S), :len(S)] = np.diag(S)
    A_reconstructed = U @ Sigma @ Vt
    print("Reconstructed A:\n", A_reconstructed)

---

## 7. Do It Yourself 🚀
1. Perform SVD on  

   $$
   A = \begin{bmatrix}
   2 & 4 \\
   1 & 3 \\
   0 & 0
   \end{bmatrix}
   $$  

   and verify $A = U \Sigma V^T$.  

2. In Python, generate a random $4 \times 3$ matrix and compute its SVD.  

3. Verify that columns of $U$ are orthonormal ($U^T U = I$).  

---

## 8. Memory Tips 🧠
- SVD = “rotate → stretch → rotate.”  
- $\Sigma$ = strengths of transformations (singular values).  
- $U$ and $V$ = orthogonal “directions.”  
- Similar to PCA but works directly on any $m \times n$ matrix.  

---

✅ By the end of this section, you should understand:
- What SVD is and how it factorizes matrices  
- How to compute SVD step by step  
- Applications of SVD in ML and DS  
- How to implement SVD in Python  

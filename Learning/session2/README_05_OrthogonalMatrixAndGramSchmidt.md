# README_05_OrthogonalMatrixAndGramSchmidt

## 📌 Syllabus Coverage
This README covers the following from **Session 2 (Linear Transformations)**:
- Orthogonal matrix
- Gram–Schmidt Process

---

## 1. Orthogonal Matrix

### Definition
A square matrix $Q$ is **orthogonal** if its rows and columns are orthonormal vectors.  
That is:

$$
Q^T Q = Q Q^T = I
$$

### Properties
- $Q^{-1} = Q^T$  
- $\det(Q) = \pm 1$  
- Orthogonal transformations preserve **lengths** and **angles**.  
- Common examples: rotations, reflections.  

### Example
$$
Q = \begin{bmatrix}
0 & -1 \\
1 & 0
\end{bmatrix}, \quad
Q^T Q = I
$$

---

## 2. Gram–Schmidt Process

### Definition
The Gram–Schmidt process converts a set of linearly independent vectors into an **orthogonal (or orthonormal) set**.  

### Steps
Given vectors $u_1, u_2, \dots, u_n$:  

1. Set $v_1 = \dfrac{u_1}{\|u_1\|}$  
2. Subtract projections of $u_2$ on $v_1$, normalize → $v_2$  
3. Subtract projections of $u_3$ on $v_1, v_2$, normalize → $v_3$  
4. Continue until all $u_i$ are processed.  

Formally:  

$$
w_k = u_k - \sum_{j=1}^{k-1} \text{proj}_{v_j}(u_k), \quad v_k = \frac{w_k}{\|w_k\|}
$$

Where projection is:  

$$
\text{proj}_{v}(u) = \frac{u \cdot v}{v \cdot v} v
$$

---

## 3. Coding Hint (Python)
    import numpy as np

    def gram_schmidt(A):
        """Orthonormalize the columns of matrix A using Gram-Schmidt."""
        Q = np.zeros_like(A, dtype=float)
        for i in range(A.shape[1]):
            v = A[:, i]
            for j in range(i):
                v -= np.dot(Q[:, j], A[:, i]) * Q[:, j]
            Q[:, i] = v / np.linalg.norm(v)
        return Q

    # Example
    A = np.array([[2, 2, 4],
                  [0, 3, 5],
                  [0, 4, 5]])
    Q = gram_schmidt(A)
    print("Orthonormal basis:\n", Q)
    print("Check Q^T Q = I:\n", Q.T @ Q)

---

## 4. Do It Yourself 🚀
1. Verify that for the $2 \times 2$ rotation matrix  

   $$
   R = \begin{bmatrix}
   \cos\theta & -\sin\theta \\
   \sin\theta & \cos\theta
   \end{bmatrix}
   $$  

   we have $R^T R = I$.  

2. Apply Gram–Schmidt on the vectors $(1,1,0)$ and $(1,0,1)$, and compute the resulting orthonormal basis.  

3. In Python, generate a random $3 \times 3$ matrix and orthonormalize its columns.  

---

## 5. Memory Tips 🧠
- Orthogonal = “transpose = inverse.”  
- Gram–Schmidt = “subtract shadows, then normalize.”  
- Think of Gram–Schmidt as making vectors **perpendicular friends**.  

---

✅ By the end of this section, you should understand:
- What orthogonal matrices are and their properties  
- How orthogonal transformations preserve geometry  
- How the Gram–Schmidt process generates orthonormal bases  
- How to implement Gram–Schmidt in Python  

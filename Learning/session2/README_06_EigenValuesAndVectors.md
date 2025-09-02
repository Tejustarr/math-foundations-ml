# README_06_EigenValuesAndVectors

## 📌 Syllabus Coverage
This README covers the following from **Session 2 (Linear Transformations)**:
- Eigenvalues and Eigenvectors

---

## 1. Definition
For a square matrix $A$, a non-zero vector $v$ is called an **eigenvector** if:

$$
A v = \lambda v
$$

where $\lambda$ is a scalar called the **eigenvalue** corresponding to $v$.  

- Eigenvector: the direction that does not change under transformation $A$.  
- Eigenvalue: the factor by which the eigenvector is stretched or compressed.  

---

## 2. Finding Eigenvalues
From the equation:

$$
A v = \lambda v
$$

Rearranging:

$$
(A - \lambda I)v = 0
$$

For non-trivial solutions,  

$$
\det(A - \lambda I) = 0
$$

This is called the **characteristic equation**, whose roots are the eigenvalues.  

---

## 3. Finding Eigenvectors
Once eigenvalues $\lambda$ are found, substitute each into:

$$
(A - \lambda I)v = 0
$$

to solve for the corresponding eigenvectors $v$.  

---

## 4. Example
Let  

$$
A = \begin{bmatrix}
2 & 1 \\
1 & 1
\end{bmatrix}
$$

Characteristic equation:

$$
\det(A - \lambda I) = 
\begin{vmatrix}
2 - \lambda & 1 \\
1 & 1 - \lambda
\end{vmatrix}
= (2-\lambda)(1-\lambda) - 1 = 0
$$

Solve:  

$$
\lambda^2 - 3\lambda + 1 = 0
$$

Eigenvalues:  

$$
\lambda_1 = \frac{3 + \sqrt{5}}{2}, \quad 
\lambda_2 = \frac{3 - \sqrt{5}}{2}
$$

Eigenvectors are found by solving $(A - \lambda I)v = 0$ for each $\lambda$.  

---

## 5. Coding Hint (Python)
    import numpy as np

    A = np.array([[2, 1],
                  [1, 1]])

    # Eigenvalues and Eigenvectors
    eigvals, eigvecs = np.linalg.eig(A)
    print("Eigenvalues:", eigvals)
    print("Eigenvectors:\n", eigvecs)

---

## 6. Do It Yourself 🚀
1. Compute the eigenvalues and eigenvectors of  

   $$
   \begin{bmatrix}
   4 & 2 \\
   1 & 3
   \end{bmatrix}
   $$  

2. Verify in Python that $A v = \lambda v$ for one eigenpair.  

3. Generate a random $3 \times 3$ matrix in Python and compute its eigenvalues and eigenvectors using `np.linalg.eig`.  

---

## 7. Memory Tips 🧠
- **Eigen = special/characteristic.**  
- Equation: $Av = \lambda v$ → “same direction, scaled length.”  
- Solve $\det(A - \lambda I) = 0$ to find eigenvalues.  

---

✅ By the end of this section, you should understand:
- What eigenvalues and eigenvectors are  
- How to compute them mathematically  
- How to implement their calculation in Python  

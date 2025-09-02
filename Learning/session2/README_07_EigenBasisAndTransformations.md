# README_07_EigenBasisAndTransformations

## 📌 Syllabus Coverage
This README covers the following from **Session 2 (Linear Transformations)**:
- Eigenbasis and Transformations

---

## 1. Definition
If a matrix $A$ has $n$ linearly independent eigenvectors, they can form a **basis** of $\mathbb{R}^n$, called the **eigenbasis**.  

In this basis, $A$ acts like a diagonal matrix, which simplifies many computations.  

---

## 2. Diagonalization
A square matrix $A$ can be written as:

$$
A = E D E^{-1}
$$

Where:  
- $E$ = matrix of eigenvectors (columns are eigenvectors).  
- $D$ = diagonal matrix of eigenvalues.  

---

## 3. Powers of a Matrix
Using diagonalization:

$$
A^n = E D^n E^{-1}
$$

Since $D$ is diagonal, $D^n$ is easy to compute by raising each diagonal entry to the $n$-th power.  

---

## 4. Example
Let  

$$
A = \begin{bmatrix}
2 & 1 \\
1 & 1
\end{bmatrix}
$$

Suppose its eigenvectors form $E$ and eigenvalues form $D$.  

Then:

$$
A = E D E^{-1}
$$

and for any power:

$$
A^k = E D^k E^{-1}
$$

---

## 5. Coding Hint (Python)
    import numpy as np

    A = np.array([[2, 1],
                  [1, 1]])

    eigvals, eigvecs = np.linalg.eig(A)

    # Form matrices
    D = np.diag(eigvals)
    E = eigvecs
    E_inv = np.linalg.inv(E)

    # Reconstruct A
    A_reconstructed = E @ D @ E_inv
    print("Reconstructed A:\n", A_reconstructed)

    # Compute A^5 using diagonalization
    D_power = np.diag(eigvals**5)
    A_power = E @ D_power @ E_inv
    print("A^5:\n", A_power)

---

## 6. Do It Yourself 🚀
1. Diagonalize  

   $$
   \begin{bmatrix}
   4 & 1 \\
   2 & 3
   \end{bmatrix}
   $$  

   and verify $A = E D E^{-1}$.  

2. Compute $A^4$ using diagonalization.  

3. In Python, generate a $3 \times 3$ symmetric matrix and diagonalize it using `np.linalg.eig`.  

---

## 7. Memory Tips 🧠
- Diagonalization = “matrix in its simplest form.”  
- Columns of $E$ = eigenvectors.  
- $D$ = eigenvalues on the diagonal.  
- Easy powers: $A^n = E D^n E^{-1}$.  

---

✅ By the end of this section, you should understand:
- What an eigenbasis is  
- How matrices can be diagonalized  
- How diagonalization simplifies computations  
- How to implement diagonalization in Python  

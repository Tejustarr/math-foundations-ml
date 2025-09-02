# README_04_DeterminantAndInverseForSpecialMatrices

## 📌 Syllabus Coverage
This README covers the following from **Session 2 (Linear Transformations)**:
- Determinant and Inverse for Special Matrices

---

## 1. Special Matrices Overview
Certain types of matrices have simplified rules for computing determinants and inverses.  
Recognizing these can save time in both theory and computation.

---

## 2. Determinants of Special Matrices
1. **Triangular Matrix (Upper/Lower)**  
   - Determinant = product of diagonal entries.  
   $$
   \det \begin{bmatrix}
   2 & 3 & 1 \\
   0 & 5 & 4 \\
   0 & 0 & 6
   \end{bmatrix} = 2 \cdot 5 \cdot 6 = 60
   $$

2. **Diagonal Matrix**  
   - Determinant = product of diagonal elements.  

3. **Orthogonal Matrix**  
   - Determinant = $\pm 1$.  

---

## 3. Inverses of Special Matrices
1. **Diagonal Matrix**  
   - Inverse is obtained by taking reciprocals of diagonal elements.  
   $$
   D = \begin{bmatrix}
   2 & 0 & 0 \\
   0 & 5 & 0 \\
   0 & 0 & 10
   \end{bmatrix}, \quad
   D^{-1} = \begin{bmatrix}
   \tfrac{1}{2} & 0 & 0 \\
   0 & \tfrac{1}{5} & 0 \\
   0 & 0 & \tfrac{1}{10}
   \end{bmatrix}
   $$

2. **Orthogonal Matrix ($Q$)**  
   - $Q^{-1} = Q^T$.  

3. **Triangular Matrix**  
   - Inverse can be found using back-substitution (if diagonal entries are non-zero).  

---

## 4. Coding Hint (Python)
    import numpy as np

    # Diagonal matrix
    D = np.diag([2, 5, 10])
    print("Determinant (Diagonal):", np.linalg.det(D))
    print("Inverse (Diagonal):\n", np.linalg.inv(D))

    # Orthogonal matrix example (rotation 90°)
    Q = np.array([[0, -1],
                  [1,  0]])
    print("Determinant (Orthogonal):", np.linalg.det(Q))
    print("Q^T == Q^-1 ?", np.allclose(Q.T, np.linalg.inv(Q)))

    # Upper triangular matrix
    U = np.array([[2, 3, 1],
                  [0, 5, 4],
                  [0, 0, 6]])
    print("Determinant (Upper Triangular):", np.linalg.det(U))

---

## 5. Do It Yourself 🚀
1. Compute the determinant of a $4 \times 4$ diagonal matrix with diagonal entries $(1,2,3,4)$.  
2. Verify in Python that for an orthogonal matrix $Q$, $Q^T = Q^{-1}$.  
3. Take a $3 \times 3$ upper triangular matrix and check if its determinant equals the product of diagonal entries.  

---

## 6. Memory Tips 🧠
- **Triangular**: determinant = product of diagonal.  
- **Diagonal**: inverse = reciprocals of diagonal.  
- **Orthogonal**: inverse = transpose.  
- Shortcut: “Special structure → simple formula.”  

---

✅ By the end of this section, you should understand:
- How determinants behave for special matrices  
- How to compute inverses more easily for diagonal, triangular, and orthogonal matrices  
- How to verify these properties in Python  

# README_03_MatrixInverse

## 📌 Syllabus Coverage
This README covers the following from **Session 2 (Linear Transformations)**:
- Matrix Inverse

---

## 1. Definition
The **inverse of a matrix** $A$, denoted $A^{-1}$, is a matrix such that:

$$
A A^{-1} = A^{-1} A = I
$$

where $I$ is the identity matrix.  

- Only **square matrices** can have inverses.  
- A matrix is invertible (non-singular) if $\det(A) \neq 0$.  

---

## 2. Properties of Inverse
- $(A^{-1})^{-1} = A$  
- $(AB)^{-1} = B^{-1}A^{-1}$  
- $(A^T)^{-1} = (A^{-1})^T$  

---

## 3. Solving Systems of Equations
If $AX = B$, multiplying both sides by $A^{-1}$:

$$
X = A^{-1}B
$$

This provides the solution vector $X$.  

---

## 4. Physical Meaning
- A matrix $A$ represents a **transformation**.  
- The inverse matrix $A^{-1}$ **reverses** that transformation.  
- Example: If $A$ rotates a vector by $90^\circ$, then $A^{-1}$ rotates it by $-90^\circ$.  

---

## 5. Methods to Compute Inverse
1. **Formula for $2 \times 2$ Matrix**  

If  

$$
A = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix},
$$  

then  

$$
A^{-1} = \frac{1}{ad - bc} \begin{bmatrix}
d & -b \\
-c & a
\end{bmatrix}
$$

2. **General Method**: Gaussian elimination or row reduction.  
3. **Using NumPy**: `np.linalg.inv(A)`.  

---

## 6. Coding Hint (Python)
    import numpy as np

    # Example matrix
    A = np.array([[2, 1],
                  [7, 4]])

    # Inverse
    inv_A = np.linalg.inv(A)
    print("Inverse of A:\n", inv_A)

    # Verify A * A^-1 = I
    I = A @ inv_A
    print("Verification (A * A^-1):\n", I)

---

## 7. Do It Yourself 🚀
1. Compute the inverse of  

   $$
   \begin{bmatrix}
   4 & 7 \\
   2 & 6
   \end{bmatrix}
   $$  

   Verify that $AA^{-1} = I$.  

2. In Python, generate a random $3 \times 3$ matrix (with non-zero determinant) and compute its inverse.  

3. Verify $(AB)^{-1} = B^{-1}A^{-1}$ using two random invertible matrices.  

---

## 8. Memory Tips 🧠
- Determinant $\neq 0$ → Invertible.  
- Inverse = **“undo”** the effect of a matrix.  
- Formula for $2 \times 2$: **swap diagonal, flip signs of off-diagonal, divide by determinant**.  

---

✅ By the end of this section, you should understand:
- What a matrix inverse is  
- When it exists  
- How to compute and interpret it  
- How to use inverse matrices to solve systems in Python  

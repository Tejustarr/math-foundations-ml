# README_02_Determinant

## 📌 Syllabus Coverage
This README covers the following from **Session 2 (Linear Transformations)**:
- Determinant (definition, calculation, geometric meaning, scaling effect)

---

## 1. Definition
The **determinant** of a square matrix is a scalar value that summarizes key properties of the matrix, such as invertibility and geometric scaling.  

For a matrix $A$, determinant is denoted as $\det(A)$ or $|A|$.

---

## 2. Calculation Rules
### (a) Determinant of a $2 \times 2$ Matrix
For  

$$
A = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix},
$$  

the determinant is  

$$
\det(A) = ad - bc
$$

---

### (b) Determinant of a $3 \times 3$ Matrix
For  

$$
A = \begin{bmatrix}
a & b & c \\
d & e & f \\
g & h & i
\end{bmatrix},
$$  

the determinant is  

$$
\det(A) = a(ei - fh) - b(di - fg) + c(dh - eg)
$$

---

## 3. Geometric Interpretation
- The determinant represents the **scaling factor** of area (2D) or volume (3D) when a transformation matrix is applied.  
- $\det(A) = 0$ → The transformation squashes space into a lower dimension (not invertible).  
- $\det(A) < 0$ → The transformation **flips orientation**.  
- $\det(A) > 0$ → Orientation is preserved.  

Examples:
- In **2D**: Determinant = area scaling factor.  
- In **3D**: Determinant = volume scaling factor.  

---

## 4. Coding Hint (Python)
    import numpy as np

    # 2x2 matrix
    A = np.array([[2, 3],
                  [1, 4]])
    print("Determinant (2x2):", np.linalg.det(A))

    # 3x3 matrix
    B = np.array([[2, 3, 4],
                  [3, 4, 5],
                  [5, 6, 3]])
    print("Determinant (3x3):", np.linalg.det(B))

---

## 5. Do It Yourself 🚀
1. Compute the determinant of:  

   $$
   \begin{bmatrix}
   1 & 2 \\
   3 & 4
   \end{bmatrix}
   $$  

2. Find the determinant of:  

   $$
   \begin{bmatrix}
   2 & 0 & 1 \\
   -1 & 3 & 2 \\
   3 & 1 & 0
   \end{bmatrix}
   $$  

3. In Python, generate a random $4 \times 4$ matrix and compute its determinant using `np.linalg.det`.  

---

## 6. Memory Tips 🧠
- $2 \times 2$: **criss-cross multiply → subtract** ($ad - bc$).  
- $3 \times 3$: **“plus, minus, plus” rule** for expansion.  
- Determinant = **scaling factor** (area/volume).  

---

✅ By the end of this section, you should understand:
- What a determinant is  
- How to compute determinants of $2 \times 2$ and $3 \times 3$ matrices  
- The geometric meaning of determinants  
- How to compute determinants in Python  

# README_07_TypesOfMatrix

## 📌 Syllabus Coverage
This README covers the following from **Session 1 (Introduction to Linear Algebra)**:
- Types of Matrix

---

## 1. Definition
A **matrix type** refers to a matrix with specific structural properties that make it useful in mathematics and applications.  
Recognizing matrix types helps simplify problems and computations.  

---

## 2. Common Types of Matrices
1. **Row Matrix**  
   - Only one row.  
   - Example: $\begin{bmatrix} 1 & 2 & 3 \end{bmatrix}$  

2. **Column Matrix**  
   - Only one column.  
   - Example: $\begin{bmatrix} 4 \\ 5 \\ 6 \end{bmatrix}$  

3. **Square Matrix**  
   - Rows = Columns.  
   - Example: $3 \times 3$ matrix.  

4. **Diagonal Matrix**  
   - All non-diagonal elements are zero.  
   - Example: $\begin{bmatrix} 2 & 0 & 0 \\ 0 & 5 & 0 \\ 0 & 0 & 7 \end{bmatrix}$  

5. **Identity Matrix ($I$)**  
   - Square matrix with 1’s on diagonal, 0’s elsewhere.  
   - Example: $\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$  

6. **Zero Matrix**  
   - All elements are zero.  

7. **Triangular Matrices**  
   - **Upper Triangular**: All elements below diagonal are zero.  
     $\begin{bmatrix} 1 & 2 & 3 \\ 0 & 4 & 5 \\ 0 & 0 & 6 \end{bmatrix}$  
   - **Lower Triangular**: All elements above diagonal are zero.  
     $\begin{bmatrix} 1 & 0 & 0 \\ 2 & 3 & 0 \\ 4 & 5 & 6 \end{bmatrix}$  

8. **Symmetric Matrix**  
   - $A = A^T$ (mirror along diagonal).  

9. **Skew-Symmetric Matrix**  
   - $A^T = -A$.  

10. **Orthogonal Matrix**  
    - $A^TA = AA^T = I$.  

11. **Sparse Matrix**  
    - Most entries are zero. Common in data science (e.g., user-item ratings).  

---

## 3. Coding Hint (Python)
    import numpy as np

    # Identity matrix
    I = np.eye(3)
    print("Identity matrix:\n", I)

    # Diagonal matrix
    D = np.diag([2, 5, 7])
    print("Diagonal matrix:\n", D)

    # Upper triangular matrix
    U = np.array([[1, 2, 3],
                  [0, 4, 5],
                  [0, 0, 6]])
    print("Upper triangular:\n", U)

    # Check if symmetric
    A = np.array([[1, 2],
                  [2, 1]])
    print("Is A symmetric?", np.allclose(A, A.T))

---

## 4. Do It Yourself 🚀
1. Construct a $3 \times 3$ symmetric matrix in Python.  
   - Verify that $A = A^T$.  

2. Create a random $3 \times 3$ matrix and check if it is orthogonal by verifying $A^TA = I$.  

3. Generate a $5 \times 5$ sparse matrix with mostly zeros (e.g., only 3 non-zero entries).  

---

## 5. Memory Tips 🧠
- Identity matrix = “do nothing” matrix.  
- Symmetric = “mirror across diagonal.”  
- Orthogonal = “special rotations/reflections.”  
- Sparse = “mostly zeros.”  

---

✅ By the end of this section, you should understand:
- Different types of matrices and their properties  
- How to identify them mathematically  
- How to construct and verify them in Python  

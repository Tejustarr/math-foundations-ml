# README_01_LinearAlgebraOverview

## 📌 Syllabus Coverage
This README covers the following from **Session 1 (Introduction to Linear Algebra)**:
- Linear Algebra Overview

---

## 1. Definition
Linear Algebra is the branch of mathematics that studies **vectors, matrices, and linear transformations**.  
It provides tools to represent data, perform transformations, and solve systems of linear equations.

A **linear equation** has the form:

$$
a_1x_1 + a_2x_2 + \dots + a_nx_n = b
$$

---

## 2. Why Linear Algebra Matters in Data Science & ML
- Data is represented in **vectors and matrices**.  
- Many ML methods rely on **linear transformations**.  
- Solving systems of equations is the basis for algorithms like regression and PCA.  

---

## 3. Key Formula / Representation
Consider the system:

$$
\begin{aligned}
2a + 3b + 4c &= 11 \\
3a + 5b + 5c &= 15 \\
5a + 6b + 3c &= 19
\end{aligned}
$$

In **matrix form**:

$$
AX = B
$$

Where:

$$
A = \begin{bmatrix} 
2 & 3 & 4 \\ 
3 & 5 & 5 \\ 
5 & 6 & 3 
\end{bmatrix}, \quad
X = \begin{bmatrix} 
a \\ b \\ c 
\end{bmatrix}, \quad
B = \begin{bmatrix} 
11 \\ 15 \\ 19 
\end{bmatrix}
$$

---

## 4. Coding Hint (Python)
    import numpy as np

    # Coefficient matrix A
    A = np.array([[2, 3, 4],
                  [3, 5, 5],
                  [5, 6, 3]])

    # Result vector B
    B = np.array([11, 15, 19])

    # Solve AX = B
    X = np.linalg.solve(A, B)
    print("Solution for [a, b, c]:", X)

---

## 5. Do It Yourself 🚀
1. Represent and solve the following system in matrix form:

   $$
   \begin{aligned}
   x + y + z &= 6 \\
   2y + 5z &= -4 \\
   2x + 5y - z &= 27
   \end{aligned}
   $$

2. Create a $4 \times 4$ random matrix using NumPy and compute its transpose.

---

## 6. Memory Tips 🧠
- Think: **Equation → Matrix → Solution**.  
- Shortcut: **AX = B** = “All (A) times X gives B”.  
- Linear Algebra is the **language of data**.  

---

✅ By the end of this section, you should understand:
- What Linear Algebra is  
- Why it is important in ML & Data Science  
- How to represent equations as matrices  
- How to solve simple systems in Python  

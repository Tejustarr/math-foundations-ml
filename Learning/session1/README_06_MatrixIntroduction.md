# README_06_MatrixIntroduction

## 📌 Syllabus Coverage
This README covers the following from **Session 1 (Introduction to Linear Algebra)**:
- Matrix Introduction

---

## 1. Definition
A **matrix** is a rectangular array of numbers arranged in **rows** and **columns**.  

Example of a $3 \times 3$ matrix:

$$
A = \begin{bmatrix} 
a_{11} & a_{12} & a_{13} \\ 
a_{21} & a_{22} & a_{23} \\ 
a_{31} & a_{32} & a_{33} 
\end{bmatrix}
$$

---

## 2. Key Concepts
- **Matrix Dimensions**: A matrix with $m$ rows and $n$ columns is called an $m \times n$ matrix.  
- **Row Vector**: A $1 \times n$ matrix.  
- **Column Vector**: An $m \times 1$ matrix.  
- **Square Matrix**: Number of rows = number of columns.  

---

## 3. Basic Matrix Operations
1. **Addition / Subtraction**:  
   Two matrices of the same size can be added/subtracted element-wise.  

   $$
   A + B = \begin{bmatrix} 
   a_{11} + b_{11} & a_{12} + b_{12} \\ 
   a_{21} + b_{21} & a_{22} + b_{22} 
   \end{bmatrix}
   $$

2. **Scalar Multiplication**:  
   Multiply every element by a scalar $k$.  

   $$
   kA = \begin{bmatrix} 
   ka_{11} & ka_{12} \\ 
   ka_{21} & ka_{22} 
   \end{bmatrix}
   $$

3. **Matrix Multiplication**:  
   If $A$ is $m \times n$ and $B$ is $n \times p$, then $AB$ is $m \times p$.  

   $$
   C_{ij} = \sum_{k=1}^{n} A_{ik}B_{kj}
   $$

---

## 4. Matrix Properties
- Associative: $(AB)C = A(BC)$  
- Distributive: $A(B+C) = AB + AC$  
- Identity Matrix $I$: $AI = IA = A$  
- Transpose: $(A^T)_{ij} = A_{ji}$  

---

## 5. Coding Hint (Python)
    import numpy as np

    # Define two matrices
    A = np.array([[1, 2],
                  [3, 4]])

    B = np.array([[5, 6],
                  [7, 8]])

    # Addition
    print("A + B =\n", A + B)

    # Scalar multiplication
    print("2 * A =\n", 2 * A)

    # Matrix multiplication
    print("A @ B =\n", A @ B)

    # Transpose
    print("Transpose of A =\n", A.T)

---

## 6. Do It Yourself 🚀
1. Create two $3 \times 3$ matrices in Python and:  
   - Add them  
   - Multiply one by a scalar  
   - Compute their matrix product  

2. Write the $2 \times 2$ identity matrix and verify $AI = IA = A$.  

---

## 7. Memory Tips 🧠
- Matrix = “table of numbers.”  
- Rule of multiplication: **columns of left = rows of right**.  
- Think of multiplication as **row by column dot products**.  

---

✅ By the end of this section, you should understand:
- What a matrix is  
- Matrix dimensions and types  
- Basic matrix operations and properties  
- How to implement matrix operations in Python  

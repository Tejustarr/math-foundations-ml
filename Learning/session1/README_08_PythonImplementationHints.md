# README_08_PythonImplementationHints

## 📌 Syllabus Coverage
This README covers the following from **Session 1 (Introduction to Linear Algebra)**:
- Implementation in Python

---

## 1. Overview
Python, with libraries like **NumPy**, provides efficient tools for performing linear algebra operations.  
NumPy’s `linalg` module includes functions for solving systems, computing norms, dot products, projections, and more.

---

## 2. Common Functions
1. **Vector Norms**
    
    ```bash
    import numpy as np
    u = np.array([3, 4])
    print("Euclidean norm:", np.linalg.norm(u))       # L2
    print("Manhattan norm:", np.linalg.norm(u, ord=1)) # L1
    ```

2. **Dot Product**
    
    ```bash
    a = np.array([1, 2, 3])
    b = np.array([4, 5, 6])
    print("Dot product:", np.dot(a, b))
    ```

3. **Scalar and Vector Projection**
    
    ```bash
    u = np.array([2, 3])
    v = np.array([1, 0])

    # Scalar projection of u on v
    sc_proj = np.dot(u, v) / np.linalg.norm(v)
    print("Scalar projection:", sc_proj)

    # Vector projection of u on v
    vec_proj = (np.dot(u, v) / np.linalg.norm(v)**2) * v
    print("Vector projection:", vec_proj)
    ```

4. **Matrix Inverse**
    
    ```bash
    A = np.array([[2, 1],
                  [7, 4]])
    inv_A = np.linalg.inv(A)
    print("Inverse of A:\n", inv_A)
    ```

5. **Solving Linear Systems**
    
    ```bash
    A = np.array([[2, 3, 4],
                  [3, 5, 5],
                  [5, 6, 3]])
    B = np.array([11, 15, 19])
    X = np.linalg.solve(A, B)
    print("Solution [a, b, c]:", X)
    ```

---

## 3. Do It Yourself 🚀
1. Compute the dot product of two random 5D vectors in Python.  
2. Create a random $3 \times 3$ matrix, compute its determinant and inverse.  
3. Verify that $A \cdot A^{-1} = I$ for a non-singular square matrix.  

---

## 4. Memory Tips 🧠
- NumPy module: `np.linalg` = “Linear Algebra functions.”  
- Use `@` for matrix multiplication in Python (e.g., `A @ B`).  
- Always check determinant $\neq 0$ before inverting a matrix.  

---

✅ By the end of this section, you should understand:
- How to use NumPy for vector and matrix operations  
- How to compute norms, projections, and inverses in Python  
- How to solve linear systems with `np.linalg.solve`  

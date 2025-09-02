# 📘 Session 1 — Matrix Introduction

This file introduces **matrices**, their notation, operations, and basic properties with examples and Python hints.

---

## 🔹 1. What is a Matrix?

* **Definition:** A 2D array (rectangular grid) of numbers arranged in rows and columns.
* Notation: Uppercase letters (A, B, M).
* Dimensions: m × n (m rows, n columns).

**Example:**

$$
A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}
$$

* A is a 2×3 matrix.

---

## 🔹 2. Types of Matrix Elements

* **Entry aᵢⱼ:** element at row i, column j.
* Example: in A above, a₂₃ = 6 (row 2, col 3).

---

## 🔹 3. Special Cases

* **Row matrix:** 1×n (single row).
* **Column matrix:** n×1 (single column).
* **Square matrix:** n×n (rows = columns).

---

## 🔹 4. Basic Matrix Operations

### a) Addition & Subtraction

* Only valid if matrices have same dimensions.

$$
(A + B)_{ij} = a_{ij} + b_{ij}
$$

### b) Scalar Multiplication

$$
cA = (c a_{ij})
$$

### c) Matrix Multiplication

* If A is (m×n), B is (n×p), then C = AB is (m×p):

$$
C_{ij} = \sum_{k=1}^n a_{ik} b_{kj}
$$

* **Note:** Multiplication is **not commutative** (AB ≠ BA in general).

### d) Transpose

* Flip rows and columns.

$$
A^T_{ij} = A_{ji}
$$

---

## 🔹 5. Properties of Matrix Operations

* Associativity: (AB)C = A(BC)
* Distributivity: A(B+C) = AB + AC
* Non-commutativity: AB ≠ BA (generally)
* Identity element: AI = A = IA

---

## 🔹 6. Python Hints

```python
import numpy as np

# Define matrices
A = np.array([[1,2,3],[4,5,6]])
B = np.array([[7,8,9],[10,11,12]])

# Addition, scalar mult
print(A + B)
print(2 * A)

# Matrix multiplication
C = np.array([[1,2],[3,4],[5,6]])
print(A @ C)   # (2x3)@(3x2) → (2x2)

# Transpose
print(A.T)
```

---

## ✅ Quick Recap

* Matrix = 2D array (m×n).
* Elements indexed as aᵢⱼ.
* Operations: add, scalar mult, matrix mult, transpose.
* Properties: associative, distributive, non-commutative.
* Python: use `@` for multiplication, `.T` for transpose.

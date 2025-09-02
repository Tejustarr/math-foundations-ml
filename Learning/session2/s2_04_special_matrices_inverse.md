# 📘 Session 2 — Determinant & Inverse for Special Matrices

This file explains how the **determinant and inverse** behave for special classes of matrices, with properties and shortcuts.

---

## 🔹 1. Diagonal Matrices

* Form: only diagonal elements may be non-zero.

$$
D = \begin{bmatrix} d_1 & 0 & 0 \\ 0 & d_2 & 0 \\ 0 & 0 & d_3 \end{bmatrix}
$$

* Determinant:

$$
\det(D) = d_1 d_2 d_3
$$

* Inverse:

$$
D^{-1} = \begin{bmatrix} 1/d_1 & 0 & 0 \\ 0 & 1/d_2 & 0 \\ 0 & 0 & 1/d_3 \end{bmatrix}, \quad \text{if all } d_i \neq 0
$$

**Python Hint:**

```python
import numpy as np
D = np.diag([2,3,4])
print(np.linalg.det(D))
print(np.linalg.inv(D))
```

---

## 🔹 2. Triangular Matrices

* **Upper triangular:** all entries below diagonal = 0.

* **Lower triangular:** all entries above diagonal = 0.

* Determinant = product of diagonal entries.

* Inverse (if exists): also triangular of same type.

**Python Hint:**

```python
U = np.array([[2,1,0],[0,3,4],[0,0,5]])
print(np.linalg.det(U))  # 2*3*5 = 30
```

---

## 🔹 3. Orthogonal Matrices

* Definition: Q is orthogonal if $Q^T Q = I$.
* Determinant:

$$
\det(Q) = \pm 1
$$

* Inverse:

$$
Q^{-1} = Q^T
$$

**Python Hint:**

```python
Q = np.array([[0,1],[-1,0]])
print(np.linalg.det(Q))   # -1
print(np.allclose(Q.T, np.linalg.inv(Q)))  # True
```

---

## 🔹 4. Singular Matrices

* If det(A)=0 → matrix is **singular** (non-invertible).
* Occurs when rows/columns are linearly dependent.

---

## ✅ Quick Recap

* Diagonal/triangular: det = product of diagonal entries; inverse easy if diagonals ≠ 0.
* Orthogonal: inverse = transpose, det = ±1.
* Singular matrices have no inverse (det=0).

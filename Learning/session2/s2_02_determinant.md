# 📘 Session 2 — Determinant

This file introduces the **determinant** of a matrix: definition, formulas, intuition, and Python hints.

---

## 🔹 1. What is a Determinant?

* A scalar value associated with a **square matrix**.
* Denoted det(A) or |A|.
* Tells us about invertibility, scaling, and orientation.

---

## 🔹 2. Determinant of 2×2 Matrix

For matrix:

$$
A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}
$$

Formula:

$$
\det(A) = ad - bc
$$

---

## 🔹 3. Determinant of 3×3 Matrix

For matrix:

$$
A = \begin{bmatrix} a & b & c \\ d & e & f \\ g & h & i \end{bmatrix}
$$

Formula (expansion):

$$
\det(A) = a(ei - fh) - b(di - fg) + c(dh - eg)
$$

---

## 🔹 4. General Definition

* Defined via **cofactor expansion** (Laplace expansion).
* Or as product of eigenvalues.
* More generally, determinant = signed volume scaling factor of transformation.

---

## 🔹 5. Properties of Determinant

1. det(I) = 1 (identity matrix).
2. det(AB) = det(A) det(B).
3. det(Aᵀ) = det(A).
4. det(A)=0 → A is singular (non-invertible).
5. Swapping two rows flips sign.
6. Multiplying row by scalar multiplies determinant by same scalar.

---

## 🔹 6. Intuition

* In 2D: det = area scaling factor.

  * Example: |det|=2 → area doubled.
  * det < 0 → reflection (orientation flipped).
* In 3D: det = volume scaling factor.

---

## 🔹 7. Python Hints

```python
import numpy as np

# 2x2 determinant
A = np.array([[2,3],[1,4]])
print(np.linalg.det(A))  # 5

# 3x3 determinant
B = np.array([[1,2,3],[0,1,4],[5,6,0]])
print(np.linalg.det(B))
```

---

## ✅ Quick Recap

* Determinant = scalar linked to square matrix.
* 2×2: ad−bc, 3×3: expansion formula.
* Properties: det(AB)=det(A)det(B), det=0 → not invertible.
* Intuition: area/volume scaling + orientation flip.

# 📘 Session 2 — Matrix Inverse

This file introduces the **matrix inverse**, its definition, formulas, conditions for existence, and Python hints.

---

## 🔹 1. What is the Inverse of a Matrix?

* For a square matrix A, the **inverse** A⁻¹ is defined such that:

$$
A A^{-1} = A^{-1} A = I
$$

where I is the identity matrix.

* Not all matrices are invertible.

---

## 🔹 2. Conditions for Invertibility

* A must be **square** (n×n).
* det(A) ≠ 0.
* Rank(A) = n.
* Such matrices are called **non-singular**.

If det(A)=0 → A is singular (no inverse).

---

## 🔹 3. Inverse of a 2×2 Matrix

For matrix:

$$
A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}
$$

Formula:

$$
A^{-1} = \frac{1}{ad - bc} \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}
$$

---

## 🔹 4. Methods for Finding Inverse

1. **Adjoint & Determinant (cofactor method)**
2. **Row-reduction (Gaussian elimination)**
3. **LU decomposition** (computationally efficient)

---

## 🔹 5. Properties of Inverses

1. (A⁻¹)⁻¹ = A.
2. (AB)⁻¹ = B⁻¹ A⁻¹.
3. (Aᵀ)⁻¹ = (A⁻¹)ᵀ.
4. Orthogonal matrices: A⁻¹ = Aᵀ.

---

## 🔹 6. Geometric Meaning

* Inverse “reverses” the transformation done by A.
* If A scales space by factor k, then A⁻¹ scales by 1/k.
* If A rotates by θ, A⁻¹ rotates by –θ.

---

## 🔹 7. Python Hints

```python
import numpy as np

# 2x2 example
A = np.array([[2,3],[1,4]])
A_inv = np.linalg.inv(A)
print(A_inv)

# Verify A @ A_inv = I
print(A @ A_inv)
```

---

## ✅ Quick Recap

* Inverse exists only for non-singular square matrices (det≠0).
* 2×2 formula: (1/(ad−bc))\[\[d,−b],\[−c,a]].
* Found using cofactors, elimination, or decompositions.
* Geometric meaning: undoes the effect of the transformation.

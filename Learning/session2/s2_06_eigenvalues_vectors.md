# 📘 Session 2 — Eigenvalues and Eigenvectors

This file introduces **eigenvalues and eigenvectors**, their definitions, computation, meaning, and Python hints.

---

## 🔹 1. Definition

For a square matrix A:

$$
A v = \lambda v
$$

* v ≠ 0 is an **eigenvector**.
* λ is the corresponding **eigenvalue**.

---

## 🔹 2. Characteristic Equation

To find eigenvalues:

$$
\det(A - \lambda I) = 0
$$

* Roots λ = eigenvalues.
* Substitute back to find eigenvectors.

---

## 🔹 3. Example (2×2)

$$
A = \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}
$$

Characteristic polynomial:

$$
\det\begin{bmatrix} 2-\lambda & 1 \\ 1 & 2-\lambda \end{bmatrix} = (2-\lambda)^2 - 1 = 0
$$

$$
\lambda^2 - 4\lambda + 3 = 0 \implies \lambda_1=3, \; \lambda_2=1
$$

Eigenvectors:

* For λ=3: solve (A−3I)v=0 → v₁=\[1,1].
* For λ=1: solve (A−I)v=0 → v₂=\[1,−1].

---

## 🔹 4. Properties

1. If A is n×n, it has ≤ n eigenvalues.
2. Sum of eigenvalues = trace(A).
3. Product of eigenvalues = det(A).
4. Eigenvectors corresponding to distinct eigenvalues are linearly independent.
5. For symmetric A: eigenvalues are real, eigenvectors orthogonal.

---

## 🔹 5. Geometric Meaning

* Eigenvector = direction that remains unchanged after transformation.
* Eigenvalue = factor by which vector is stretched/shrunk.
* Example: reflection matrix has eigenvectors along axis of reflection.

---

## 🔹 6. Python Hints

```python
import numpy as np

A = np.array([[2,1],[1,2]])
eigvals, eigvecs = np.linalg.eig(A)
print("Eigenvalues:", eigvals)
print("Eigenvectors:\n", eigvecs)
```

---

## ✅ Quick Recap

* Eigenpair (λ,v): Av=λv.
* Solve det(A−λI)=0 for eigenvalues.
* Eigenvectors: solve (A−λI)v=0.
* Geometric view: eigenvector = unchanged direction, λ = scaling factor.
* Useful in PCA, stability analysis, PageRank, quantum mechanics.

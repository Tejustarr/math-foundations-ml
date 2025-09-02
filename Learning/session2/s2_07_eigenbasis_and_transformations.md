# 📘 Session 2 — Eigenbasis and Transformations

This file explains **eigenbasis**, diagonalization, and transformations using eigenvalues and eigenvectors.

---

## 🔹 1. Eigenbasis

* A set of eigenvectors that forms a basis of the vector space.
* If A has n linearly independent eigenvectors, they can be arranged into matrix E:

$$
E = [v_1, v_2, …, v_n]
$$

---

## 🔹 2. Diagonalization

If A has n independent eigenvectors:

$$
A = E D E^{-1}
$$

* D = diagonal matrix of eigenvalues.

* E = matrix of eigenvectors.

* Powers of A become easy:

$$
A^k = E D^k E^{-1}
$$

---

## 🔹 3. Example

$$
A = \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}
$$

* Eigenvalues: λ₁=3, λ₂=1.
* Eigenvectors: v₁=\[1,1], v₂=\[1,−1].

So:

$$
E = \begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix}, \quad D = \begin{bmatrix}3 & 0 \\ 0 & 1\end{bmatrix}
$$

Then:

$$
A = E D E^{-1}
$$

---

## 🔹 4. Geometric Meaning

* Diagonalization = change of basis into eigenbasis.
* In eigenbasis:

  * A simply scales each axis by eigenvalue.
* Useful for simplifying repeated applications of A (powers, exponentials).

---

## 🔹 5. Applications

* PCA: project data into eigenbasis of covariance matrix.
* Differential equations: solve systems using diagonalization.
* Markov chains: steady state from eigenvalue 1.

---

## 🔹 6. Python Hints

```python
import numpy as np

A = np.array([[2,1],[1,2]])
eigvals, eigvecs = np.linalg.eig(A)
E = eigvecs
D = np.diag(eigvals)

# Verify A = E D E^-1
A_reconstructed = E @ D @ np.linalg.inv(E)
print(np.allclose(A, A_reconstructed))  # True
```

---

## ✅ Quick Recap

* Eigenbasis = eigenvectors form basis.
* Diagonalization: A=EDE⁻¹.
* Simplifies matrix powers: Aᵏ=EDᵏE⁻¹.
* Applications: PCA, differential equations, Markov chains.

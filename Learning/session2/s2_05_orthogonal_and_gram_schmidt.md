# 📘 Session 2 — Orthogonal Matrices & Gram–Schmidt Process

This file covers **orthogonal matrices** and the **Gram–Schmidt process** for building an orthonormal basis.

---

## 🔹 1. Orthogonal Matrices

* A square matrix Q is **orthogonal** if:

$$
Q^T Q = I
$$

* Properties:

  1. Columns (and rows) form an **orthonormal basis**.
  2. Preserve vector lengths and angles.
  3. det(Q) = ±1.
  4. Inverse = transpose: Q⁻¹ = Qᵀ.

**Example:** 90° rotation matrix:

$$
Q = \begin{bmatrix}0 & -1 \\ 1 & 0\end{bmatrix}, \quad Q^T Q = I
$$

**Python Hint:**

```python
import numpy as np
Q = np.array([[0,-1],[1,0]])
print(Q.T @ Q)   # identity
print(np.allclose(np.linalg.inv(Q), Q.T))  # True
```

---

## 🔹 2. Why Orthonormal Bases?

* Make computations simpler:

  * Length = sqrt(sum of squares).
  * Coordinates of vector = dot products with basis vectors.
* In ML: used in PCA, QR decomposition, optimization.

---

## 🔹 3. Gram–Schmidt Process

Transforms a set of linearly independent vectors into an **orthonormal basis**.

### Steps (for {u₁, u₂, …, uₖ}):

1. Let v₁ = u₁ / ‖u₁‖.
2. Subtract projection of u₂ on v₁:

   $$
   u₂' = u₂ - (u₂·v₁)v₁, \quad v₂ = u₂'/‖u₂'‖
   $$
3. For general uₖ:

   $$
   uₖ' = uₖ - \sum_{j=1}^{k-1}(uₖ·vⱼ)vⱼ, \quad vₖ = uₖ'/‖uₖ'‖
   $$

Result: {v₁, v₂, …, vₖ} = orthonormal basis.

---

## 🔹 4. Example

Given u₁ = (1,1,0), u₂ = (1,0,1):

1. v₁ = u₁ / ‖u₁‖ = (1/√2)(1,1,0).
2. u₂' = u₂ - (u₂·v₁)v₁.

   * Compute projection → subtract → normalize.

---

## 🔹 5. Python Hints

```python
import numpy as np

def gram_schmidt(V):
    U = []
    for v in V:
        for u in U:
            v = v - np.dot(v,u)*u   # subtract projections
        v = v / np.linalg.norm(v)   # normalize
        U.append(v)
    return np.array(U)

V = np.array([[1,1,0],[1,0,1]], dtype=float)
print(gram_schmidt(V))
```

---

## ✅ Quick Recap

* Orthogonal matrices: QᵀQ=I, preserve lengths/angles, inverse=transpose.
* Orthonormal basis = independent, orthogonal, unit length.
* Gram–Schmidt = systematic way to orthonormalize vectors.

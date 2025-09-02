# 📘 Session 1 — Linear Independence, Span, and Basis

This file explains **linear combinations, dependence, independence, span, and basis** of vectors, with formulas and Python hints.

---

## 🔹 1. Linear Combination

* A vector **v** is a linear combination of vectors u₁, u₂, …, uₖ if:

$$
v = c_1 u_1 + c_2 u_2 + … + c_k u_k
$$

where c₁, c₂, … are scalars.

**Example:**

$$
(3,4) = 3(1,0) + 4(0,1)
$$

---

## 🔹 2. Linear Dependence

* A set of vectors is **linearly dependent** if one vector can be expressed as a linear combination of others.
* Equivalently: there exist scalars, not all zero, such that:

$$
c_1 u_1 + c_2 u_2 + … + c_k u_k = 0
$$

**Example:** \[2,4] is dependent on \[1,2] because \[2,4] = 2×\[1,2].

---

## 🔹 3. Linear Independence

* Vectors are **independent** if the only solution to:

$$
c_1 u_1 + c_2 u_2 + … + c_k u_k = 0
$$

is c₁ = c₂ = … = cₖ = 0.

* Intuition:

  * Independent = provide “new directions” in space.
  * Dependent = redundant.

---

## 🔹 4. Span

* The **span** of a set of vectors = all possible linear combinations of them.

**Example:**

* Span(\[1,0],\[0,1]) = all of ℝ² (the plane).
* Span(\[1,2]) = line through origin in ℝ².

---

## 🔹 5. Basis

* A **basis** of a vector space = minimal set of linearly independent vectors that span the space.
* Dimension = number of vectors in basis.

**Examples:**

* Standard basis of ℝ²: { \[1,0], \[0,1] }
* Standard basis of ℝ³: { \[1,0,0], \[0,1,0], \[0,0,1] }

---

## 🔹 6. Orthonormal Basis

* Basis vectors that are **orthogonal** (dot product = 0) and have **unit norm**.
* Useful for simplifying computations.

**Example:**

$$
\{ (1,0), (0,1) \}
$$

is orthonormal basis of ℝ².

---

## 🔹 7. Python Hints

```python
import numpy as np

# Check linear dependence using rank
u = np.array([[1,2],[2,4]])   # two vectors as columns
print(np.linalg.matrix_rank(u))  # 1 → dependent, not 2

# Standard basis in R^3
E = np.eye(3)
print(E)
```

---

## ✅ Quick Recap

* **Linear combination:** weighted sum of vectors.
* **Dependence:** one vector redundant.
* **Independence:** all directions unique.
* **Span:** all possible linear combinations.
* **Basis:** minimal independent set spanning space.
* **Orthonormal basis:** independent + orthogonal + unit length.

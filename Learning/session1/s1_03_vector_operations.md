# 📘 Session 1 — Vector Operations

This file covers **vector operations** from Session 1 (Introduction to Linear Algebra). It includes definitions, formulas, intuition, and Python code hints.

---

## 🔹 1. Vector Addition & Subtraction

* **Definition:** Combine vectors component-wise.

$$
(u + v)_i = u_i + v_i \quad , \quad (u - v)_i = u_i - v_i
$$

* **Geometric meaning:** Head-to-tail rule → forms a parallelogram.

**Python Hint:**

```python
import numpy as np
u = np.array([2, 3])
v = np.array([1, -1])
print(u + v)   # [3 2]
print(u - v)   # [1 4]
```

---

## 🔹 2. Scalar Multiplication

* **Definition:** Multiply each entry of vector by scalar $c$.

$$
c u = (c u_1, c u_2, …, c u_n)
$$

**Python Hint:**

```python
c = 3
print(c * u)  # [6 9]
```

---

## 🔹 3. Norms (Vector Length)

* **L2 norm (Euclidean):**

$$
\|u\|_2 = \sqrt{u_1^2 + u_2^2 + … + u_n^2}
$$

* **L1 norm (Manhattan):**

$$
\|u\|_1 = |u_1| + |u_2| + … + |u_n|
$$

* **General p-norm:**

$$
\|u\|_p = \left( \sum_{i=1}^n |u_i|^p \right)^{1/p}
$$

**Python Hint:**

```python
print(np.linalg.norm(u))       # L2 norm
print(np.linalg.norm(u, 1))    # L1 norm
print(np.linalg.norm(u, np.inf))  # Infinity norm
```

---

## 🔹 4. Dot Product

* **Definition:**

$$
u · v = \sum_{i=1}^n u_i v_i
$$

* **Geometric meaning:**

$$
u · v = \|u\| \|v\| \cos \theta
$$

where θ = angle between u and v.

* If u·v = 0 → vectors are orthogonal.

**Python Hint:**

```python
print(np.dot(u, v))
```

---

## 🔹 5. Cross Product (3D only)

* **Definition:** For u, v ∈ ℝ³, result = vector orthogonal to both.

$$
u × v = (u_2 v_3 - u_3 v_2, \; u_3 v_1 - u_1 v_3, \; u_1 v_2 - u_2 v_1)
$$

* Magnitude = area of parallelogram spanned by u, v.

**Python Hint:**

```python
u3 = np.array([1,2,3])
v3 = np.array([4,5,6])
print(np.cross(u3, v3))  # [-3  6 -3]
```

---

## 🔹 6. Projection

* **Scalar projection of u on v:**

$$
\text{scal}_{u→v} = \frac{u·v}{\|v\|}
$$

* **Vector projection of u on v:**

$$
\text{proj}_v(u) = \frac{u·v}{v·v} v
$$

* **Orthogonal component:**

$$
u_⊥ = u - \text{proj}_v(u)
$$

**Python Hint:**

```python
u = np.array([3,4])
v = np.array([1,0])
proj_v = (np.dot(u,v) / np.dot(v,v)) * v
print(proj_v)  # [3. 0.]
```

---

## ✅ Quick Recap

* Addition/subtraction = combine component-wise.
* Norm = length (L2 most common).
* Dot product = similarity & angle relation.
* Cross product = perpendicular vector in 3D.
* Projection = shadow of one vector onto another.

# 📘 Session 1 — Scalars, Vectors, Matrices, and Tensors

This file introduces the **basic objects** of Linear Algebra: scalars, vectors, matrices, and tensors, with definitions, properties, and Python hints.

---

## 🔹 1. Scalars

* **Definition:** A single number (magnitude only).
* Examples: temperature = 30, age = 25.
* Denoted usually by lowercase letters (a, b, c).

---

## 🔹 2. Vectors

* **Definition:** Ordered list of numbers; has magnitude and direction.
* Represented as 1D arrays.
* Can be column (n×1) or row (1×n).

**Example:**

$$
\vec{v} = \begin{bmatrix}2 \\ 5 \\ -3\end{bmatrix}
$$

* Dimension = number of components (e.g., ℝ³ for 3D vector).
* Geometric view: arrow in space.

**Python Hint:**

```python
import numpy as np
v = np.array([2, 5, -3])
print(v.shape)   # (3,) → vector in R^3
```

---

## 🔹 3. Matrices

* **Definition:** 2D array of numbers (rectangular grid).
* Denoted by uppercase letters (A, B, M).
* Size: m × n (m rows, n columns).

**Example:**

$$
A = \begin{bmatrix}1 & 2 & 3 \\ 4 & 5 & 6\end{bmatrix}
$$

* Here, A is 2×3 matrix.

* **Row vector:** 1×n matrix.

* **Column vector:** n×1 matrix.

**Python Hint:**

```python
A = np.array([[1,2,3],[4,5,6]])
print(A.shape)  # (2, 3)
```

---

## 🔹 4. Tensors

* **Definition:** Generalization of scalars, vectors, and matrices to higher dimensions.
* 0D = scalar, 1D = vector, 2D = matrix, nD = tensor.
* Widely used in deep learning (e.g., PyTorch, TensorFlow).

**Example:**

* Grayscale image (28×28) = 2D matrix.
* RGB image (28×28×3) = 3D tensor.

**Python Hint:**

```python
img_gray = np.random.rand(28,28)       # matrix (2D)
img_rgb = np.random.rand(28,28,3)      # tensor (3D)
```

---

## 🔹 5. Summary Table

| Object | Dimension | Example              | Python Shape |
| ------ | --------- | -------------------- | ------------ |
| Scalar | 0D        | 7                    | ()           |
| Vector | 1D        | \[2,5,-3]            | (3,)         |
| Matrix | 2D        | \[\[1,2,3],\[4,5,6]] | (2,3)        |
| Tensor | 3D+       | RGB image 28×28×3    | (28,28,3)    |

---

## ✅ Quick Recap

* Scalar = single value.
* Vector = 1D array, has direction + magnitude.
* Matrix = 2D array, table of numbers.
* Tensor = generalized nD array (images, deep learning).

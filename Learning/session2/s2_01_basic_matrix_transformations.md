# 📘 Session 2 — Basic Matrix Transformations

This file introduces **basic linear transformations** using matrices: scaling, reflection, projection, and rotation.

---

## 🔹 1. What is a Linear Transformation?

* A linear transformation maps a vector to another vector using a matrix.

$$
T(x) = A x
$$

* Matrix A encodes the transformation.
* Preserves vector addition and scalar multiplication.

---

## 🔹 2. Scaling

* Stretches or shrinks space along coordinate axes.

**Matrix form (2D):**

$$
S = \begin{bmatrix} s_x & 0 \\ 0 & s_y \end{bmatrix}
$$

* Effect: (x, y) → (sₓx, sᵧy).

**Example:** Double x, halve y:

$$
\begin{bmatrix}2 & 0 \\ 0 & 0.5\end{bmatrix}
$$

**Python Hint:**

```python
import numpy as np
S = np.array([[2,0],[0,0.5]])
v = np.array([1,2])
print(S @ v)  # [2, 1]
```

---

## 🔹 3. Reflection

* Flips vectors across a line/axis.

* Across x-axis:

$$
R_x = \begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix}
$$

* Across y-axis:

$$
R_y = \begin{bmatrix}-1 & 0 \\ 0 & 1\end{bmatrix}
$$

* Through origin:

$$
R_o = \begin{bmatrix}-1 & 0 \\ 0 & -1\end{bmatrix}
$$

**Python Hint:**

```python
R = np.array([[1,0],[0,-1]])
v = np.array([2,3])
print(R @ v)  # [ 2 -3]
```

---

## 🔹 4. Projection

* Projects a vector onto a subspace (e.g., x-axis).

* Projection onto x-axis:

$$
P_x = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix}
$$

* Projection onto y-axis:

$$
P_y = \begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix}
$$

**General formula (projection of u onto v):**

$$
\text{proj}_v(u) = \frac{u·v}{v·v} v
$$

**Python Hint:**

```python
u = np.array([3,4])
v = np.array([1,0])
proj_v = (np.dot(u,v)/np.dot(v,v))*v
print(proj_v)  # [3. 0.]
```

---

## 🔹 5. Rotation

* Rotates vectors by angle θ around origin.

**Matrix (2D):**

$$
R_\theta = \begin{bmatrix}\cos\theta & -\sin\theta \\ \sin\theta & \cos\theta\end{bmatrix}
$$

* Example: 90° rotation (θ=π/2):

$$
R_{90} = \begin{bmatrix}0 & -1 \\ 1 & 0\end{bmatrix}
$$

**Python Hint:**

```python
theta = np.pi/2
R = np.array([[np.cos(theta), -np.sin(theta)],
              [np.sin(theta),  np.cos(theta)]])
v = np.array([1,0])
print(R @ v)  # [0. 1]
```

---

## ✅ Quick Recap

* **Scaling:** stretch/compress axes.
* **Reflection:** flip across axis/origin.
* **Projection:** shadow onto axis/subspace.
* **Rotation:** rotate around origin by θ.

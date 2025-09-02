# 📘 Session 1 — Types of Matrices

This file introduces **different classes of matrices**, their properties, and Python hints.

---

## 🔹 1. Identity Matrix

* Square matrix with 1’s on diagonal, 0’s elsewhere.

$$
I = \begin{bmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{bmatrix}
$$

* Property: AI = A = IA.

**Python Hint:**

```python
import numpy as np
I = np.eye(3)
print(I)
```

---

## 🔹 2. Diagonal Matrix

* Only diagonal entries may be non-zero.

$$
D = \begin{bmatrix}d_1 & 0 & 0 \\ 0 & d_2 & 0 \\ 0 & 0 & d_3\end{bmatrix}
$$

* Special case: scalar matrix (all diagonal elements equal).

**Python Hint:**

```python
D = np.diag([2,4,6])
```

---

## 🔹 3. Symmetric Matrix

* A = Aᵀ.
* Example:

$$
A = \begin{bmatrix}1 & 2 \\ 2 & 3\end{bmatrix}
$$

**Python Hint:**

```python
A = np.array([[1,2],[2,3]])
print(np.allclose(A, A.T))  # True
```

---

## 🔹 4. Triangular Matrices

* **Upper triangular:** entries below diagonal = 0.

$$
U = \begin{bmatrix}1 & 2 & 3 \\ 0 & 4 & 5 \\ 0 & 0 & 6\end{bmatrix}
$$

* **Lower triangular:** entries above diagonal = 0.

**Python Hint:**

```python
U = np.triu([[1,2,3],[4,5,6],[7,8,9]])
L = np.tril([[1,2,3],[4,5,6],[7,8,9]])
```

---

## 🔹 5. Orthogonal Matrix

* Square matrix Q where:

$$
Q^T Q = I
$$

* Columns/rows form orthonormal basis.
* Preserves lengths and angles.
* Property: inverse = transpose.

**Python Hint:**

```python
Q = np.array([[0,1],[-1,0]])  # 90-degree rotation
print(Q.T @ Q)  # identity
```

---

## 🔹 6. Sparse Matrix

* Mostly zeros, few non-zero elements.
* Efficient storage with `scipy.sparse`.

**Python Hint:**

```python
from scipy.sparse import csr_matrix
A = csr_matrix([[1,0,0],[0,0,2],[0,0,0]])
print(A)
```

---

## ✅ Quick Recap

* Identity: 1’s on diagonal, multiplicative identity.
* Diagonal: only diagonal non-zero.
* Symmetric: A = Aᵀ.
* Triangular: upper or lower form.
* Orthogonal: preserves length, QᵀQ=I.
* Sparse: mostly zeros, stored efficiently.

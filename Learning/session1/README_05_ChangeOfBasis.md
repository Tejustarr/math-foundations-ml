# README_05_ChangeOfBasis

## 📌 Syllabus Coverage
This README covers the following from **Session 1 (Introduction to Linear Algebra)**:
- Change of basis (Vector)

---

## 1. Definition
A **basis** of a vector space is a set of linearly independent vectors that can represent every vector in the space as a linear combination of them.  

A **change of basis** is the process of converting the representation of a vector from one basis to another.  

---

## 2. Why Change of Basis?
- Provides a new perspective or simpler representation of data.  
- Useful in **dimensionality reduction** (e.g., PCA chooses a new basis aligned with maximum variance).  
- Helps simplify computations in different coordinate systems.  

---

## 3. Mathematical Explanation
Suppose $\{ \vec{e}_1, \vec{e}_2 \}$ is the **old basis** and $\{ \vec{b}_1, \vec{b}_2 \}$ is the **new basis** of $\mathbb{R}^2$.  

If a vector $\vec{v}$ has coordinates $[v]_B$ in the new basis, then its coordinates in the standard basis are:

$$
\vec{v} = P [v]_B
$$

Where:  
- $P$ is the **change of basis matrix**, whose columns are the new basis vectors expressed in the old basis.  

To switch back:

$$
[v]_B = P^{-1} \vec{v}
$$

---

## 4. Example
Let the new basis vectors be:

$$
\vec{b}_1 = \begin{bmatrix} 1 \\ 1 \end{bmatrix}, \quad
\vec{b}_2 = \begin{bmatrix} -1 \\ 1 \end{bmatrix}
$$

Then the change of basis matrix is:

$$
P = \begin{bmatrix} 1 & -1 \\ 1 & 1 \end{bmatrix}
$$

If $\vec{v} = \begin{bmatrix} 2 \\ 3 \end{bmatrix}$ in the standard basis,  
its coordinates in the new basis are:

$$
[v]_B = P^{-1}\vec{v}
$$

---

## 5. Coding Hint (Python)
    import numpy as np

    # New basis vectors
    b1 = np.array([1, 1])
    b2 = np.array([-1, 1])

    # Change of basis matrix
    P = np.column_stack((b1, b2))

    # Vector in standard basis
    v = np.array([2, 3])

    # Coordinates in new basis
    v_new = np.linalg.inv(P) @ v
    print("Coordinates in new basis:", v_new)

---

## 6. Do It Yourself 🚀
1. Let $\vec{b}_1 = (2,0)$ and $\vec{b}_2 = (0,3)$.  
   - Construct the change of basis matrix.  
   - Express $\vec{v} = (4,6)$ in this new basis.  

2. In Python, generate two random 2D basis vectors, form $P$, and convert a random vector into the new basis.  

---

## 7. Memory Tips 🧠
- Think: **“Change of Glasses” → Change of Basis.**  
- Columns of $P$ = new basis vectors.  
- Forward: $\vec{v} = P[v]_B$  
- Backward: $[v]_B = P^{-1}\vec{v}$  

---

✅ By the end of this section, you should understand:
- What a basis is  
- What it means to change basis  
- How to mathematically perform a basis change  
- How to implement change of basis in Python  

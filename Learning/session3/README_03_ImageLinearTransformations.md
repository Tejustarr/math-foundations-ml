# README_03_ImageLinearTransformations

## 📌 Syllabus Coverage
This README covers the following from **Session 3 (Linear Algebra Applications)**:
- Image Linear Transformations
- Affine transformations (rotation, scaling, reflection, translation)
- Inverse transforms

---

## 1. Definition
A **linear (or affine) transformation** in image processing is the mapping of pixel coordinates using a transformation matrix.  

General affine transformation in 2D (homogeneous coordinates):

$$
\begin{bmatrix}
x' \\
y' \\
1
\end{bmatrix}
=
T
\begin{bmatrix}
x \\
y \\
1
\end{bmatrix}
$$

where $T$ is a $3 \times 3$ transformation matrix.

---

## 2. Common Transformations

### (a) Identity
Leaves the image unchanged:  

$$
I = \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

---

### (b) Translation
Shifts the image by $(t_x, t_y)$:  

$$
T = \begin{bmatrix}
1 & 0 & t_x \\
0 & 1 & t_y \\
0 & 0 & 1
\end{bmatrix}
$$

---

### (c) Scaling
Scales along $x$ and $y$ by factors $s_x, s_y$:  

$$
S = \begin{bmatrix}
s_x & 0 & 0 \\
0 & s_y & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

---

### (d) Rotation
Rotates image by $\theta$ (in radians):  

$$
R = \begin{bmatrix}
\cos\theta & -\sin\theta & 0 \\
\sin\theta & \cos\theta  & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

---

### (e) Reflection
Flips image across axis:  

- About x-axis: $\begin{bmatrix} 1 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$  
- About y-axis: $\begin{bmatrix} -1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$  
- About origin: $\begin{bmatrix} -1 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$  

---

## 3. Inverse Transform
- To **undo** a transformation, use the inverse of its matrix.  
- If $T$ is invertible, then:  

$$
\vec{x} = T^{-1} \vec{x'}
$$

Example: Scaling by $s_x=2, s_y=2$ can be reversed by scaling with $1/2$.  

---

## 4. Coding Hint (Python)
    import numpy as np

    # Example: 2D point
    v = np.array([1, 2, 1])  # homogeneous coordinates

    # Translation by (2,3)
    T = np.array([[1, 0, 2],
                  [0, 1, 3],
                  [0, 0, 1]])
    print("Translated:", T @ v)

    # Rotation 90 degrees
    theta = np.pi / 2
    R = np.array([[np.cos(theta), -np.sin(theta), 0],
                  [np.sin(theta),  np.cos(theta), 0],
                  [0, 0, 1]])
    print("Rotated:", R @ v)

    # Scaling by 2
    S = np.array([[2, 0, 0],
                  [0, 2, 0],
                  [0, 0, 1]])
    print("Scaled:", S @ v)

---

## 5. Do It Yourself 🚀
1. Apply a translation $(t_x=5, t_y=2)$ to the point $(3,4)$.  
2. Rotate the point $(1,0)$ by $45^\circ$.  
3. Scale a point $(2,3)$ by $(s_x=0.5, s_y=2)$.  
4. Verify in Python that applying a transform and its inverse brings the point back.  

---

## 6. Memory Tips 🧠
- Translation → “move.”  
- Scaling → “stretch/shrink.”  
- Rotation → “spin.”  
- Reflection → “flip.”  
- Inverse → “undo.”  

---

✅ By the end of this section, you should understand:
- How affine transformations work on images  
- How to represent translation, scaling, rotation, and reflection with matrices  
- How to compute and apply inverse transformations  
- How to implement image transformations in Python  

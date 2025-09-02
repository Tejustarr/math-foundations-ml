# README_01_BasicMatrixTransformations

## 📌 Syllabus Coverage
This README covers the following from **Session 2 (Linear Transformations)**:
- Basic Matrix Transformations (Scale, Reflection, Projection, Rotation)

---

## 1. Definition
A **transformation matrix** is a matrix that maps one vector to another.  
Applying the matrix changes the coordinates of a vector or an object.

For a vector $\vec{v}$ and transformation matrix $T$:

$$
\vec{v'} = T \cdot \vec{v}
$$

---

## 2. Types of Basic Transformations

### (a) Scale Transformation
- Expands or contracts a vector along coordinate axes.
- For 2D scaling with scale factors $s_x, s_y$:

$$
S = \begin{bmatrix}
s_x & 0 \\
0 & s_y
\end{bmatrix}
$$

Example: $s_x = 2, s_y = 1.5$

$$
S = \begin{bmatrix}
2 & 0 \\
0 & 1.5
\end{bmatrix}
$$

---

### (b) Reflection Transformation
- Produces a mirror image of a vector across an axis or the origin.

Reflection matrices in 2D:

- About **x-axis**: $\begin{bmatrix} 1 & 0 \\ 0 & -1 \end{bmatrix}$  
- About **y-axis**: $\begin{bmatrix} -1 & 0 \\ 0 & 1 \end{bmatrix}$  
- About **origin**: $\begin{bmatrix} -1 & 0 \\ 0 & -1 \end{bmatrix}$  

---

### (c) Projection Transformation
- Projects vectors onto a subspace (e.g., line or axis).
- Example: Projection onto x-axis:

$$
P = \begin{bmatrix}
1 & 0 \\
0 & 0
\end{bmatrix}
$$

---

### (d) Rotation Transformation
- Rotates vectors about the origin by angle $\theta$ (in radians).
- 2D rotation matrix:

$$
R(\theta) = \begin{bmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta
\end{bmatrix}
$$

Example: $\theta = 45^\circ = \pi/4$

$$
R = \frac{1}{\sqrt{2}} \begin{bmatrix}
1 & -1 \\
1 & 1
\end{bmatrix}
$$

---

## 3. Coding Hint (Python)
    import numpy as np

    # Example vector
    v = np.array([2, 3])

    # Scaling
    S = np.array([[2, 0],
                  [0, 1.5]])
    print("Scaling:", S @ v)

    # Reflection about x-axis
    Rx = np.array([[1, 0],
                   [0, -1]])
    print("Reflection (x-axis):", Rx @ v)

    # Projection onto x-axis
    P = np.array([[1, 0],
                  [0, 0]])
    print("Projection:", P @ v)

    # Rotation 45 degrees
    theta = np.pi / 4
    R = np.array([[np.cos(theta), -np.sin(theta)],
                  [np.sin(theta),  np.cos(theta)]])
    print("Rotation 45°:", R @ v)

---

## 4. Do It Yourself 🚀
1. Apply a scaling transform with $s_x = 3, s_y = 0.5$ to vector $(2,4)$.  
2. Reflect vector $(1,2)$ about the y-axis.  
3. Project $(5,7)$ onto the x-axis.  
4. Rotate $(1,0)$ by $90^\circ$ and verify the result.  

---

## 5. Memory Tips 🧠
- Scaling → **Stretch or shrink**.  
- Reflection → **Flip across axis**.  
- Projection → **Shadow on axis**.  
- Rotation → **Spin around origin**.  

---

✅ By the end of this section, you should understand:
- What transformation matrices are  
- The four basic transformations (scale, reflection, projection, rotation)  
- How to apply them mathematically and in Python  

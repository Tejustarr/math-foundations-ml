# README_03_VectorPropertiesAndOperations

## 📌 Syllabus Coverage
This README covers the following from **Session 1 (Introduction to Linear Algebra)**:
- Vector properties and operations

---

## 1. Definition
A **vector** is a quantity that has both **magnitude** and **direction**.  
In mathematics, a vector is represented as an ordered list of numbers (components).

Example:  
- In 2D space: $\vec{v} = \begin{bmatrix} x \\ y \end{bmatrix}$  
- In 3D space: $\vec{v} = \begin{bmatrix} x \\ y \\ z \end{bmatrix}$  

---

## 2. Vector Properties
1. **Addition is commutative**:  
   $\vec{u} + \vec{v} = \vec{v} + \vec{u}$  

2. **Addition is associative**:  
   $(\vec{u} + \vec{v}) + \vec{w} = \vec{u} + (\vec{v} + \vec{w})$  

3. **Scalar multiplication distributive law**:  
   $a(\vec{u} + \vec{v}) = a\vec{u} + a\vec{v}$  

4. **Multiplicative identity**:  
   $1 \cdot \vec{u} = \vec{u}$  

---

## 3. Vector Operations
1. **Addition**:  

   $\vec{u} + \vec{v} = \begin{bmatrix} x_1 \\ y_1 \end{bmatrix} + \begin{bmatrix} x_2 \\ y_2 \end{bmatrix} = \begin{bmatrix} x_1 + x_2 \\ y_1 + y_2 \end{bmatrix}$  

2. **Subtraction**:  

   $\vec{u} - \vec{v} = \begin{bmatrix} x_1 - x_2 \\ y_1 - y_2 \end{bmatrix}$  

3. **Scalar Multiplication**:  

   $a\vec{u} = a \cdot \begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix} ax \\ ay \end{bmatrix}$  

4. **Dot Product (Inner Product)**:  

   $\vec{u} \cdot \vec{v} = x_1x_2 + y_1y_2$  

   - Result is a scalar  
   - Used to check orthogonality ($\vec{u} \cdot \vec{v} = 0$ means perpendicular)  

5. **Cross Product (3D only)**:  

   $\vec{u} \times \vec{v} = \begin{bmatrix} u_yv_z - u_zv_y \\ u_zv_x - u_xv_z \\ u_xv_y - u_yv_x \end{bmatrix}$  

   - Result is a vector perpendicular to both $\vec{u}$ and $\vec{v}$.  

6. **Norm (Length of a vector)**:  

   - L1 norm (Manhattan distance): $\|\vec{u}\|_1 = |x| + |y|$  
   - L2 norm (Euclidean distance): $\|\vec{u}\|_2 = \sqrt{x^2 + y^2}$  
   - General form (Minkowski): $\|\vec{u}\|_p = \big(|x_1|^p + |x_2|^p + \dots + |x_n|^p \big)^{1/p}$  

---

## 4. Coding Hint (Python)
    import numpy as np

    u = np.array([2, 3])
    v = np.array([1, 4])

    # Addition
    print("u + v =", u + v)

    # Subtraction
    print("u - v =", u - v)

    # Scalar multiplication
    print("2 * u =", 2 * u)

    # Dot product
    print("Dot product:", np.dot(u, v))

    # Norms
    print("L1 norm of u:", np.linalg.norm(u, ord=1))
    print("L2 norm of u:", np.linalg.norm(u))

---

## 5. Do It Yourself 🚀
1. Let $\vec{u} = (3,4)$ and $\vec{v} = (4,-3)$.  
   - Compute $\vec{u} \cdot \vec{v}$  
   - Verify if they are orthogonal.  

2. For $\vec{u} = (1,2,3)$ and $\vec{v} = (4,5,6)$:  
   - Compute $\vec{u} \times \vec{v}$.  

3. Generate a random 5D vector in Python and compute its L1, L2, and L∞ (Chebyshev) norms.  

---

## 6. Memory Tips 🧠
- Dot = number → **dot product gives scalar**.  
- Cross = new vector → **cross product gives perpendicular vector**.  
- “Norm = Length” → Norm measures the size of a vector.  

---

✅ By the end of this section, you should understand:
- Properties of vector operations  
- Addition, subtraction, scalar multiplication  
- Dot product, cross product, and norms  
- How to compute vector operations in Python  

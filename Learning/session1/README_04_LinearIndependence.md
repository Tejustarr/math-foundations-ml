# README_04_LinearIndependence

## 📌 Syllabus Coverage
This README covers the following from **Session 1 (Introduction to Linear Algebra)**:
- Linear Independence

---

## 1. Definition
A set of vectors is said to be **linearly independent** if **no vector in the set can be written as a linear combination of the others**.  

If at least one vector can be expressed as a combination of others, then the set is **linearly dependent**.  

Formally, vectors $\vec{v}_1, \vec{v}_2, \dots, \vec{v}_n$ are linearly independent if the equation:

$$
c_1\vec{v}_1 + c_2\vec{v}_2 + \dots + c_n\vec{v}_n = \vec{0}
$$

implies that:

$$
c_1 = c_2 = \dots = c_n = 0
$$

---

## 2. Importance
- Determines if a set of vectors provides **unique information**.  
- Identifies if vectors form a **basis** of a vector space.  
- Helps count the **number of independent equations** in a system.  
- Reduces redundancy in data representation.  

---

## 3. Examples
1. **Linearly Independent**  
   $\vec{v}_1 = (1,0)$, $\vec{v}_2 = (0,1)$  
   - Cannot express one as a multiple of the other → independent.  

2. **Linearly Dependent**  
   $\vec{v}_1 = (1,2)$, $\vec{v}_2 = (2,4)$  
   - $\vec{v}_2 = 2 \cdot \vec{v}_1$ → dependent.  

---

## 4. Mathematical Test
Vectors are linearly independent if the determinant of their matrix (when square) is **non-zero**.  

Example: For vectors $(1,2,3)$, $(4,5,6)$, and $(7,8,9)$:  

$$
A = \begin{bmatrix} 
1 & 2 & 3 \\ 
4 & 5 & 6 \\ 
7 & 8 & 9 
\end{bmatrix}
$$

Here, $\det(A) = 0$ → vectors are linearly dependent.  

---

## 5. Coding Hint (Python)
    import numpy as np

    # Example vectors as rows of matrix
    A = np.array([[1, 2, 3],
                  [4, 5, 6],
                  [7, 8, 9]])

    det_A = np.linalg.det(A)
    print("Determinant of A:", det_A)

    if np.isclose(det_A, 0):
        print("Vectors are linearly dependent")
    else:
        print("Vectors are linearly independent")

---

## 6. Do It Yourself 🚀
1. Check if the following vectors are independent:  
   $\vec{v}_1 = (2,3,1)$, $\vec{v}_2 = (4,6,2)$, $\vec{v}_3 = (1,0,1)$.  

2. Create three random $3D$ vectors in Python and check if they are linearly independent using determinant.  

3. Verify that standard basis vectors in 2D, $(1,0)$ and $(0,1)$, are linearly independent.  

---

## 7. Memory Tips 🧠
- If one vector is a **multiple** of another → Dependent.  
- Determinant $= 0$ → Dependent.  
- Determinant $\neq 0$ → Independent.  
- Think: “Independent vectors = unique directions.”  

---

✅ By the end of this section, you should understand:
- What linear independence means  
- Why it matters in vector spaces and ML  
- How to test independence mathematically  
- How to check independence in Python  

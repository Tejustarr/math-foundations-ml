# README_01_BasicTerminologies

## 📌 Syllabus Coverage
This README covers the following from **Session 5 (Functions, Derivatives and Integrals)**:
- Intervals
- Boundary and Interior Points
- n-Vectors

---

## 1. Intervals
An **interval** is a set of real numbers lying between two endpoints.  

- **Closed Interval** $[a, b]$:  
  $a \leq x \leq b$  

- **Open Interval** $(a, b)$:  
  $a < x < b$  

- **Half-Open Intervals**:  
  $[a, b)$ means $a \leq x < b$  
  $(a, b]$ means $a < x \leq b$  

- **Infinite Intervals**:  
  $(a, \infty), (-\infty, b), (-\infty, \infty)$  

---

## 2. Boundary and Interior Points
- **Interior points**: Points strictly inside an interval.  
  Example: In $[a,b]$, the interior is $(a,b)$.  

- **Boundary points**: The endpoints of the interval ($a$ and $b$).  
  - In closed interval $[a,b]$, boundaries are included.  
  - In open interval $(a,b)$, boundaries are not included.  

- **Open Interval**: all points are interior points.  
- **Closed Interval**: contains both interior and boundary points.  

---

## 3. n-Vectors
An **n-vector** is an ordered list (n-tuple) of $n$ real numbers:  

$$
\vec{x} = (x_1, x_2, \dots, x_n)
$$

- Represents a point in **n-dimensional space** ($\mathbb{R}^n$).  
- Example: $(x_1, x_2)$ → point in 2D plane.  
- Example: $(x_1, x_2, x_3)$ → point in 3D space.  

---

## 4. Coding Hint (Python)
    import numpy as np

    # Interval example: generate values in [0, 1]
    x = np.linspace(0, 1, 5)
    print("Closed interval [0,1]:", x)

    # Vector examples
    v2 = np.array([0.5, 0.7])       # 2D vector
    v3 = np.array([1, 2, 3])        # 3D vector
    v5 = np.array([1, 0, -1, 2, 4]) # 5D vector

    print("2D vector:", v2)
    print("3D vector:", v3)
    print("5D vector:", v5)

---

## 5. Do It Yourself 🚀
1. Write all types of intervals between $a=2$ and $b=5$.  
2. Identify interior and boundary points of $(0,1]$.  
3. Represent the vector $(3,4,5)$ in Python and compute its L2 norm.  

---

## 6. Memory Tips 🧠
- **Brackets [ ] = include boundaries**, **Parentheses ( ) = exclude boundaries**.  
- Open → only interior points.  
- Closed → interior + boundaries.  
- n-vector = “point in n-dimensional space.”  

---

✅ By the end of this section, you should understand:
- Different types of intervals  
- Interior vs boundary points  
- Meaning and use of n-vectors  
- How to represent intervals and vectors in Python  

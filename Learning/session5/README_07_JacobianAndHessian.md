# README_07_JacobianAndHessian

## 📌 Syllabus Coverage
This README covers the following from **Session 5 (Functions, Derivatives and Integrals)**:
- Jacobian Matrix
- Hessian Matrix

---

## 1. Jacobian Matrix

### Definition
The **Jacobian matrix** is the matrix of all **first-order partial derivatives** of a vector-valued function.

If  

$$
F(x_1, x_2, \dots, x_n) = 
\begin{bmatrix}
f_1(x_1, \dots, x_n) \\
f_2(x_1, \dots, x_n) \\
\vdots \\
f_m(x_1, \dots, x_n)
\end{bmatrix}
$$

then the Jacobian is:

$$
J = \begin{bmatrix}
\frac{\partial f_1}{\partial x_1} & \frac{\partial f_1}{\partial x_2} & \dots & \frac{\partial f_1}{\partial x_n} \\
\frac{\partial f_2}{\partial x_1} & \frac{\partial f_2}{\partial x_2} & \dots & \frac{\partial f_2}{\partial x_n} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{\partial f_m}{\partial x_1} & \frac{\partial f_m}{\partial x_2} & \dots & \frac{\partial f_m}{\partial x_n}
\end{bmatrix}
$$

### Example
For  

$$
F(x,y) = 
\begin{bmatrix}
x^2 y \\
5x + \sin y
\end{bmatrix}
$$

Jacobian:

$$
J = \begin{bmatrix}
2xy & x^2 \\
5 & \cos y
\end{bmatrix}
$$

---

## 2. Hessian Matrix

### Definition
The **Hessian matrix** is a square matrix of all **second-order partial derivatives** of a scalar-valued function.  
It describes the local curvature of a function.  

If $f(x_1, x_2, \dots, x_n)$ is scalar, then:

$$
H = \begin{bmatrix}
\frac{\partial^2 f}{\partial x_1^2} & \frac{\partial^2 f}{\partial x_1 \partial x_2} & \dots \\
\frac{\partial^2 f}{\partial x_2 \partial x_1} & \frac{\partial^2 f}{\partial x_2^2} & \dots \\
\vdots & \vdots & \ddots
\end{bmatrix}
$$

### Example
For  

$$
f(x,y) = -7x^2 - 5xy - 4y^2
$$

Hessian:

$$
H = \begin{bmatrix}
-14 & -5 \\
-5 & -8
\end{bmatrix}
$$

---

## 3. Applications
- Jacobian:  
  - Transformation of coordinates  
  - Sensitivity analysis  
  - Multivariable calculus in ML (backpropagation)  

- Hessian:  
  - Optimization (convexity/concavity tests)  
  - Newton’s method in optimization  
  - Curvature of error surfaces in ML  

---

## 4. Coding Hint (Python)
    import sympy as sp

    x, y = sp.symbols('x y')

    # Jacobian Example
    F = sp.Matrix([x**2 * y, 5*x + sp.sin(y)])
    J = F.jacobian([x, y])
    print("Jacobian:\n", J)

    # Hessian Example
    f = -7*x**2 - 5*x*y - 4*y**2
    H = sp.hessian(f, (x, y))
    print("Hessian:\n", H)

---

## 5. Do It Yourself 🚀
1. Compute Jacobian of  

   $$
   F(x,y,z) = 
   \begin{bmatrix}
   x + y \\
   yz \\
   e^x
   \end{bmatrix}
   $$  

2. Compute Hessian of $f(x,y) = x^3 + y^3 - 3xy$.  
3. Verify in Python that Hessian is symmetric.  

---

## 6. Memory Tips 🧠
- **Jacobian = first derivatives (matrix of slopes).**  
- **Hessian = second derivatives (matrix of curvature).**  
- Jacobian → vector functions, Hessian → scalar functions.  

---

✅ By the end of this section, you should understand:
- What Jacobian and Hessian matrices are  
- How to construct them mathematically  
- Their applications in optimization and ML  
- How to compute them in Python  

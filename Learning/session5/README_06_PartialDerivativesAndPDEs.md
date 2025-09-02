# README_06_PartialDerivativesAndPDEs

## 📌 Syllabus Coverage
This README covers the following from **Session 5 (Functions, Derivatives and Integrals)**:
- Partial Derivatives
- Partial Differential Equations (PDEs)

---

## 1. Partial Derivatives

### Definition
A **partial derivative** measures how a multivariable function changes with respect to one variable, while keeping others constant.

If $f(x,y)$ is a function of two variables, the partial derivatives are:

$$
\frac{\partial f}{\partial x}, \quad \frac{\partial f}{\partial y}
$$

---

### Example
For  

$$
f(x,y) = x^3 + 2x^2y + y^2 + 2x + 1
$$

- Partial derivative w.r.t $x$:  

$$
\frac{\partial f}{\partial x} = 3x^2 + 4xy + 2
$$  

- Partial derivative w.r.t $y$:  

$$
\frac{\partial f}{\partial y} = 2x^2 + 2y
$$  

---

## 2. Partial Differential Equations (PDEs)

### Definition
A **PDE** is a differential equation that involves **multivariable functions** and their partial derivatives.

General first-order PDE in $x, y$:

$$
F\left(x, y, z, \frac{\partial z}{\partial x}, \frac{\partial z}{\partial y}\right) = 0
$$

### Examples
- Heat equation:  

$$
\frac{\partial u}{\partial t} = \alpha \frac{\partial^2 u}{\partial x^2}
$$

- Wave equation:  

$$
\frac{\partial^2 u}{\partial t^2} = c^2 \frac{\partial^2 u}{\partial x^2}
$$

---

## 3. Coding Hint (Python)
    import sympy as sp

    x, y = sp.symbols('x y')
    f = x**3 + 2*x**2*y + y**2 + 2*x + 1

    # Partial derivatives
    df_dx = sp.diff(f, x)
    df_dy = sp.diff(f, y)

    print("∂f/∂x:", df_dx)
    print("∂f/∂y:", df_dy)

---

## 4. Do It Yourself 🚀
1. Compute $\partial f / \partial x$ and $\partial f / \partial y$ for  

   $$
   f(x,y) = x^2y + 3y^2
   $$  

2. Derive the heat equation $\partial u/\partial t = \alpha \, \partial^2 u/\partial x^2$ and explain each term.  

3. Use Python (SymPy) to compute $\partial f / \partial x$ for $f(x,y,z) = xyz + x^2y^2$.  

---

## 5. Memory Tips 🧠
- Symbol: $\partial$ = “partial.”  
- Hold other variables constant while differentiating.  
- PDEs model real-world systems: heat, waves, diffusion.  

---

✅ By the end of this section, you should understand:
- What partial derivatives are and how to compute them  
- Difference between ordinary derivatives and partial derivatives  
- What PDEs are and why they are important  
- How to compute partial derivatives in Python  

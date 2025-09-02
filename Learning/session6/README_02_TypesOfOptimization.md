# README_02_TypesOfOptimization

## 📌 Syllabus Coverage
This README covers the following from **Session 6 (Function Optimization)**:
- Minimization vs Maximization
- Convex and Concave Functions
- Role of Second Derivative & Hessian
- Practical Applications

---

## 1. Minimization vs Maximization
- **Minimization**: Find smallest possible value of a function.  

$$
\min_{x \in S} f(x)
$$  

Examples:  
- Cost minimization in production.  
- Loss function minimization in machine learning.  

---

- **Maximization**: Find largest possible value of a function.  

$$
\max_{x \in S} f(x)
$$  

Examples:  
- Profit maximization in business.  
- Utility maximization in economics.  

---

## 2. Convex and Concave Functions

- **Convex function**: The line segment between any two points lies **above** the graph.  
  - Condition: $f''(x) \geq 0$ for all $x$ in domain.  

$$
f(tx_1 + (1-t)x_2) \leq t f(x_1) + (1-t)f(x_2), \quad t \in [0,1]
$$  

- **Concave function**: The line segment between any two points lies **below** the graph.  
  - Condition: $f''(x) \leq 0$ for all $x$ in domain.  

---

## 3. Multivariate Case – Hessian Matrix
For $f(x_1, x_2, \dots, x_n)$, convexity/concavity depends on the **Hessian matrix** $H$ (matrix of second derivatives).  

- If $H$ is **positive semidefinite** → function is convex.  
- If $H$ is **negative semidefinite** → function is concave.  

---

## 4. Coding Hint (Python)
    import sympy as sp

    x = sp.Symbol('x')
    f = x**2 - 4*x + 3

    # First and second derivative
    f_prime = sp.diff(f, x)
    f_double_prime = sp.diff(f, x, 2)

    print("f'(x):", f_prime)
    print("f''(x):", f_double_prime)

    if f_double_prime > 0:
        print("Function is convex")
    elif f_double_prime < 0:
        print("Function is concave")
    else:
        print("Function is linear")

---

## 5. Do It Yourself 🚀
1. Check if $f(x) = x^2 + 2x + 3$ is convex or concave.  
2. Verify using second derivative that $f(x) = -x^2 + 4x$ is concave.  
3. In Python, compute Hessian of $f(x,y) = x^2 + y^2$ and check convexity.  

---

## 6. Practical Applications
- **Convex Optimization** (minimization problems):  
  - Machine learning: minimize loss functions (linear regression, logistic regression).  
  - Resource allocation & cost minimization.  

- **Concave Optimization** (maximization problems):  
  - Economics: utility maximization.  
  - Portfolio optimization in finance.  
  - Revenue/profit maximization.  

---

## 7. Memory Tips 🧠
- Convex = “bowl up” (minimization).  
- Concave = “bowl down” (maximization).  
- Second derivative test → convex ($f''>0$), concave ($f''<0$).  
- Multivariate → check Hessian.  

---

✅ By the end of this section, you should understand:
- Difference between minimization and maximization problems  
- How convexity and concavity affect optimization  
- Role of second derivative and Hessian matrix  
- Real-world applications of convex/concave optimization  

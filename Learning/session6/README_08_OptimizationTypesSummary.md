# README_08_OptimizationTypesSummary

## 📌 Syllabus Coverage (Extra from Session 6 slides)
This README extends **Session 6 (Function Optimization)** to include:
- Types of Optimization Functions

---

## 1. Constraint vs Non-Constraint Optimization
- **Constrained Optimization**: Variables must satisfy one or more constraints.  
  Example: Maximize profit subject to budget or resource limits.  

Formally:  

$$
\min f(x) \quad \text{s.t. } g_i(x) \leq 0, \; h_j(x) = 0
$$

- **Unconstrained Optimization**: No restrictions, only optimize the objective function.  
  Example: Minimize $f(x) = (x-2)^2$.  

---

## 2. Single Variable vs Multivariable
- **Single-variable optimization**: Objective depends on one variable $x$.  
  Example: $\min f(x) = x^2 - 4x + 3$  

- **Multivariable optimization**: Objective depends on multiple variables.  
  Example: $\min f(x,y) = x^2 + y^2$  

---

## 3. Discrete vs Continuous Optimization
- **Discrete Optimization**: Decision variables take integer or categorical values.  
  Example: Assigning tasks to workers (integer programming).  

- **Continuous Optimization**: Decision variables take real values.  
  Example: Minimize $f(x) = x^2 + 3x + 5$ for $x \in \mathbb{R}$.  

---

## 4. Static vs Dynamic Optimization
- **Static Optimization**: Problem parameters remain fixed.  
  Example: One-time resource allocation.  

- **Dynamic Optimization**: Problem evolves over time, requiring continual updates.  
  Example: Stock trading strategy over multiple days.  

---

## 5. Deterministic vs Stochastic Optimization
- **Deterministic Optimization**: Outcomes are certain for given inputs.  
  Example: Minimize distance in a known graph.  

- **Stochastic Optimization**: Involves randomness or uncertainty.  
  Example: Portfolio optimization under uncertain market returns.  

---

## 6. Linear vs Nonlinear Optimization
- **Linear Optimization**: Objective and constraints are linear.  
  Example: Linear programming:  

$$
\min c^T x \quad \text{s.t. } Ax \leq b
$$  

- **Nonlinear Optimization**: Objective or constraints are nonlinear.  
  Example: Minimize $f(x) = x^2 + \sin(x)$.  

---

## 7. Coding Hint (Python)
    from scipy.optimize import linprog

    # Example: Linear Programming
    # Minimize: c^T x = 2x1 + 3x2
    c = [2, 3]

    # Constraints: x1 + x2 <= 4
    A = [[1, 1]]
    b = [4]

    # Bounds: x1, x2 >= 0
    bounds = [(0, None), (0, None)]

    result = linprog(c, A_ub=A, b_ub=b, bounds=bounds, method="highs")
    print("Optimal solution:", result.x)
    print("Optimal value:", result.fun)

---

## 8. Do It Yourself 🚀
1. Formulate a constrained optimization problem for diet planning with protein and calorie limits.  
2. Create a simple **nonlinear** optimization function and check convexity.  
3. Implement a discrete optimization problem: assign 3 jobs to 3 workers with cost matrix.  

---

## 9. Memory Tips 🧠
- Constraint vs Unconstrained = “rules or no rules.”  
- Single vs Multi = “1D vs nD.”  
- Discrete vs Continuous = “integers vs real numbers.”  
- Static vs Dynamic = “fixed vs changing over time.”  
- Deterministic vs Stochastic = “certain vs uncertain.”  
- Linear vs Nonlinear = “straight lines vs curves.”  

---

✅ By the end of this section, you should understand:
- Different types of optimization problems  
- How to classify them (constraint, variable type, dynamics, randomness, linearity)  
- How these categories apply to real-world problems  
- How to implement simple optimization examples in Python  

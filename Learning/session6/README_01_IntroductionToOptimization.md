# README_01_IntroductionToOptimization

## 📌 Syllabus Coverage
This README covers the following from **Session 6 (Function Optimization)**:
- Introduction to Optimization
- Problem Formulation
- Objective Function, Variables, Constraints

---

## 1. What is Optimization?
**Optimization** is the process of finding the best possible solution under given circumstances.  
It aims to **maximize or minimize** an objective function while satisfying certain constraints.  

Formally:  

$$
\text{Find } x^* \in \mathbb{R}^n \quad \text{such that } f(x^*) \leq f(x), \; \forall x \in S
$$

for minimization problems (similar for maximization).  

---

## 2. Real-World Examples
- **Route Optimization**: minimize travel distance/time for logistics.  
- **Energy Optimization**: minimize energy consumption in industry.  
- **Revenue Maximization**: optimize product pricing/promotion in e-commerce.  
- **Supply Chain**: maximize profit while minimizing costs.  
- **Diet Planning**: maximize nutrition while minimizing calories.  

---

## 3. Elements of Optimization
1. **Objective Function $f(x)$**  
   - Function to maximize or minimize.  
   - Example: profit, cost, performance score.  

2. **Decision Variables $X = (x_1, x_2, \dots, x_n)$**  
   - Quantities we control to optimize the objective.  

3. **Constraints $g(x)$**  
   - Conditions or restrictions on variables.  
   - Example: resource limits, time limits, non-negativity.  

---

## 4. Example (Football Player Scenario)
A footballer wants to maximize performance by allocating time to sprinting ($S$), jogging ($J$), and standing ($T$).  

**Objective Function**:  

$$
\text{Performance} = 3S + 2J + 0.5T
$$

**Constraints**:  
- Match duration: $S + J + T \leq 90$  
- Energy budget: $10S + 5J + T \leq 400$  
- Non-negativity: $S, J, T \geq 0$  

Optimal solution is the feasible $(S, J, T)$ that maximizes performance.  

---

## 5. Coding Hint (Python)
    import numpy as np
    from scipy.optimize import linprog

    # Coefficients for objective (maximize 3S + 2J + 0.5T)
    c = [-3, -2, -0.5]  # negative for maximization using linprog

    # Constraints
    A = [[1, 1, 1],
         [10, 5, 1]]
    b = [90, 400]

    # Bounds for variables (non-negativity)
    bounds = [(0, None), (0, None), (0, None)]

    # Solve
    result = linprog(c, A_ub=A, b_ub=b, bounds=bounds, method="highs")
    print("Optimal values (S, J, T):", result.x)
    print("Max performance:", -result.fun)

---

## 6. Do It Yourself 🚀
1. Formulate an optimization problem for **diet planning** with 2 foods:  
   - Maximize protein, limit calories.  
2. Write the objective function, variables, and constraints.  
3. Solve a simple linear optimization problem in Python using `scipy.optimize.linprog`.  

---

## 7. Memory Tips 🧠
- **Objective = goal.**  
- **Variables = what you control.**  
- **Constraints = rules.**  
- Optimization = “best solution under restrictions.”  

---

✅ By the end of this section, you should understand:
- What optimization means  
- Objective, variables, and constraints in problem formulation  
- Real-world applications of optimization  
- How to solve a simple optimization problem in Python  

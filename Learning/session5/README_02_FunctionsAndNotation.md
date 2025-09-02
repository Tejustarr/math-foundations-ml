# README_02_FunctionsAndNotation

## 📌 Syllabus Coverage
This README covers the following from **Session 5 (Functions, Derivatives and Integrals)**:
- Definition of Functions
- Function Notation
- Graph of a Function
- Increasing and Decreasing Functions

---

## 1. Definition of a Function
A **function** is a rule that assigns each input (from a set called the **domain**) exactly one output (from a set called the **codomain**).  

If $x$ is input and $f(x)$ is output, then $f$ is the function.  

Examples:  
- Domain: $[-2,1]$, Rule: $f(x) = 2x$.  
- Domain: $(-1,1)$, Rule:  
  $$
  f(x) = \begin{cases}
  x & \text{if } x \geq 0 \\
  1/x & \text{if } x < 0
  \end{cases}
  $$

---

## 2. Function Notation
- $f : \mathbb{R}^D \to \mathbb{R}$ means $f$ maps a $D$-dimensional input to a real number.  
- Example: $f(x) = x^2 + 2x + 1$  

Each $x$ in the domain has a unique $f(x)$ in the codomain.  

---

## 3. Graph of a Function
- A function can be visualized by plotting $y = f(x)$.  
- Example:  

If $f(x) = 2x + 1$, its graph is a straight line with:  
- slope = 2  
- intercept = 1  

This is the **slope-intercept form**: $y = mx + c$.  

---

## 4. Increasing and Decreasing Functions
- **Increasing function**: $f(x_1) < f(x_2)$ whenever $x_1 < x_2$.  
- **Decreasing function**: $f(x_1) > f(x_2)$ whenever $x_1 < x_2$.  

Example:  
- $f(x) = x^2$ is increasing for $x > 0$, decreasing for $x < 0$.  

Using interval notation:  
- $f(x)$ increasing on $(2, \infty)$.  
- $f(x)$ decreasing on $(-\infty, -3)$.  

---

## 5. Coding Hint (Python)
    import numpy as np
    import matplotlib.pyplot as plt

    # Define function
    def f(x):
        return 2*x + 1

    # Values
    x = np.linspace(-5, 5, 100)
    y = f(x)

    # Plot
    plt.plot(x, y, label="f(x)=2x+1")
    plt.xlabel("x")
    plt.ylabel("f(x)")
    plt.title("Graph of f(x)")
    plt.legend()
    plt.grid(True)
    plt.show()

---

## 6. Do It Yourself 🚀
1. Write the function $f(x) = x^2 - 4x + 3$.  
   - Plot its graph and identify intervals of increase/decrease.  

2. Define a piecewise function in Python:  

   $$
   f(x) = \begin{cases}
   x^2 & x \geq 0 \\
   -x & x < 0
   \end{cases}
   $$  

   Plot the function.  

---

## 7. Memory Tips 🧠
- Function = “input → rule → output.”  
- Graph = visual representation of rule.  
- Increasing = goes **up** as $x$ increases.  
- Decreasing = goes **down** as $x$ increases.  

---

✅ By the end of this section, you should understand:
- What functions are and how to represent them  
- Function notation and mappings  
- How to interpret graphs of functions  
- Increasing and decreasing behaviors  
- How to implement and visualize functions in Python  

# README_03_IntroductionToCalculus

## 📌 Syllabus Coverage
This README covers the following from **Session 5 (Functions, Derivatives and Integrals)**:
- Introduction to Calculus
- Limits
- Differential Calculus vs Integral Calculus
- Motivation with velocity example

---

## 1. Definition
**Calculus** is the branch of mathematics that studies how functions change with respect to their input variables.  

It has two main parts:
1. **Differential Calculus** – concerned with **rates of change** (derivatives).  
2. **Integral Calculus** – concerned with **accumulation** (areas, sums, integrals).  

---

## 2. Why Calculus?
- Describes how systems change over time.  
- Used in physics, economics, biology, and machine learning.  
- Applications include:  
  - Velocity and acceleration  
  - Area under curves  
  - Optimization problems  

---

## 3. Limits
The **limit** is a fundamental idea in calculus, used to define derivatives and integrals.  

If $f(x)$ approaches $L$ as $x$ approaches $a$, we write:  

$$
\lim_{x \to a} f(x) = L
$$

Example:  

$$
\lim_{x \to 0} \frac{\sin x}{x} = 1
$$

---

## 4. Velocity Example
Suppose displacement $s(t)$ at time $t$ is given.  

- **Average velocity** over interval $[t, t+h]$:  

$$
v = \frac{s(t+h) - s(t)}{h}
$$

- **Instantaneous velocity** at $t$:  

$$
v(t) = \lim_{h \to 0} \frac{s(t+h) - s(t)}{h} = \frac{ds}{dt}
$$

This is the **derivative** of displacement with respect to time.  

---

## 5. Coding Hint (Python)
    import sympy as sp

    # Define variable and function
    t = sp.symbols('t')
    s = t**2   # displacement function

    # Derivative for velocity
    v = sp.diff(s, t)
    print("Velocity function:", v)

    # Evaluate instantaneous velocity at t=2
    v_at_2 = v.subs(t, 2)
    print("Velocity at t=2:", v_at_2)

---

## 6. Do It Yourself 🚀
1. Compute $\lim_{x \to 0} \frac{1 - \cos x}{x^2}$.  
2. If $s(t) = 3t^2 + 2t$, find velocity $v(t)$ and acceleration $a(t)$.  
3. Write Python code to compute derivative of $f(x) = \sin(x) + x^2$.  

---

## 7. Memory Tips 🧠
- Derivative = “slope” (rate of change).  
- Integral = “area” (accumulation).  
- Limit = “approach a value.”  
- Think: **Calculus = Change + Accumulation**.  

---

✅ By the end of this section, you should understand:
- What calculus studies  
- The role of limits in defining derivatives  
- Difference between differential and integral calculus  
- How velocity motivates the derivative concept  
- How to compute limits and derivatives in Python  

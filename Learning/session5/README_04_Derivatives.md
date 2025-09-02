# README_04_Derivatives

## 📌 Syllabus Coverage
This README covers the following from **Session 5 (Functions, Derivatives and Integrals)**:
- Derivatives (definition & slope interpretation)
- Concave and Convex Functions
- Differentiability conditions
- Higher-order derivatives

---

## 1. Definition
The **derivative** of a function measures the **rate of change** of the function with respect to its input variable.  

If $y = f(x)$, the derivative at $x$ is:

$$
f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}
$$

It is also written as:

- $\frac{dy}{dx}$  
- $Df(x)$  
- $\dot{y}$ (in physics, time derivatives)  

---

## 2. Derivative as Slope
- The derivative at $x = c$ is the slope of the **tangent line** to the curve at $(c, f(c))$.  
- Average slope (secant line):  

$$
m = \frac{y_2 - y_1}{x_2 - x_1}
$$  

- Instantaneous slope (tangent line):  

$$
m = \lim_{x_2 \to x_1} \frac{y_2 - y_1}{x_2 - x_1}
$$  

---

## 3. Concave and Convex Functions
- **Convex function**: slopes are **increasing** (derivative is increasing).  

$$
f(ta + (1-t)b) \leq t f(a) + (1-t) f(b)
$$  

- **Concave function**: slopes are **decreasing** (derivative is decreasing).  

---

## 4. Differentiability
A function is **differentiable at a point** if:
1. It is continuous at that point.  
2. The tangent line is not vertical.  
3. The curve is smooth (no sharp corners).  

If these fail, derivative may not exist.  

---

## 5. Higher-Order Derivatives
- **First derivative**: rate of change, slope, velocity.  
- **Second derivative**: rate of change of the first derivative (acceleration, curvature).  

$$
f''(x) = \frac{d^2y}{dx^2}
$$  

- **Third derivative**: derivative of $f''(x)$, etc.  

---

## 6. Coding Hint (Python)
    import sympy as sp

    # Define variable and function
    x = sp.symbols('x')
    f = x**3 - 3*x + 2

    # First derivative
    f_prime = sp.diff(f, x)
    print("f'(x):", f_prime)

    # Second derivative
    f_double_prime = sp.diff(f, x, 2)
    print("f''(x):", f_double_prime)

    # Evaluate derivative at x=2
    slope_at_2 = f_prime.subs(x, 2)
    print("Slope at x=2:", slope_at_2)

---

## 7. Do It Yourself 🚀
1. Compute derivative of $f(x) = x^2 + 5x + 6$.  
2. Compute second derivative of $f(x) = \sin(x) + x^3$.  
3. Plot $f(x) = x^3$ and its tangent line at $x=1$.  

---

## 8. Memory Tips 🧠
- Derivative = “instantaneous slope.”  
- 1st derivative → velocity, slope.  
- 2nd derivative → acceleration, curvature.  
- Concave up = bowl (convex), concave down = cave.  

---

✅ By the end of this section, you should understand:
- What a derivative is and how to compute it  
- The slope interpretation of derivatives  
- Concavity and convexity in functions  
- Conditions for differentiability  
- Higher-order derivatives and their meanings  
- How to compute and visualize derivatives in Python  

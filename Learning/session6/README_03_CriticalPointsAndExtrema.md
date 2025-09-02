# README_03_CriticalPointsAndExtrema

## 📌 Syllabus Coverage
This README covers the following from **Session 6 (Function Optimization)**:
- Critical Points
- Local and Global Extrema
- Saddle Points
- Second Derivative Test

---

## 1. Critical Points
A **critical point** of a function $f(x)$ occurs where:  
1. $f'(x) = 0$ (slope is zero), or  
2. $f'(x)$ is undefined.  

These points may correspond to maxima, minima, or saddle points.  

---

## 2. Local and Global Extrema
- **Local Maximum**: $f(x_0)$ is greater than nearby values.  
- **Local Minimum**: $f(x_0)$ is smaller than nearby values.  

- **Global Maximum**: $f(x_0)$ is the largest value over the entire domain.  
- **Global Minimum**: $f(x_0)$ is the smallest value over the entire domain.  

---

## 3. Saddle Points
- A **saddle point** is a critical point that is **not a max or min**.  
- In multivariable functions, it is a point where slope is zero but curvature changes direction.  

Example: $f(x,y) = x^2 - y^2$ has a saddle at $(0,0)$.  

---

## 4. Second Derivative Test
For single-variable function $f(x)$:  
1. Find critical points by solving $f'(x)=0$.  
2. Compute second derivative $f''(x)$:  
   - If $f''(x) > 0$ → local minimum.  
   - If $f''(x) < 0$ → local maximum.  
   - If $f''(x) = 0$ → test is inconclusive (could be inflection/saddle).  

For multivariable $f(x,y)$:  
- Use the **Hessian matrix** to classify critical points.  

---

## 5. Coding Hint (Python)
    import sympy as sp

    # Define variable and function
    x = sp.symbols('x')
    f = x**3 - 6*x**2 + 9*x + 1

    # First and second derivatives
    f_prime = sp.diff(f, x)
    f_double = sp.diff(f, x, 2)

    # Solve for critical points
    crit_points = sp.solve(f_prime, x)
    print("Critical points:", crit_points)

    # Classify using second derivative
    for cp in crit_points:
        test = f_double.subs(x, cp)
        if test > 0:
            print(f"{cp} -> Local Min")
        elif test < 0:
            print(f"{cp} -> Local Max")
        else:
            print(f"{cp} -> Inconclusive")

---

## 6. Do It Yourself 🚀
1. Find critical points of $f(x) = x^2 - 4x + 3$ and classify them.  
2. For $f(x) = -x^2 + 4x$, check global maximum in domain $[0,5]$.  
3. In Python, find and classify critical points of $f(x,y) = x^2 + y^2 - 4x - 6y$.  

---

## 7. Memory Tips 🧠
- Critical point = slope $=0$ or undefined.  
- $f''>0$ → convex (min).  
- $f''<0$ → concave (max).  
- Multivariable → use Hessian.  

---

✅ By the end of this section, you should understand:
- What critical points are  
- Difference between local and global extrema  
- What saddle points represent  
- How to use second derivative test to classify extrema  
- How to compute and classify critical points in Python  

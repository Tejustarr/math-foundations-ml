# README_08_ApplicationsOfDerivatives

## 📌 Syllabus Coverage
This README covers the following from **Session 5 (Functions, Derivatives and Integrals)**:
- Applications of Derivatives
- Rate of Change
- Maxima and Minima
- Tangents and Normals
- Acceleration
- Image Gradients

---

## 1. Rate of Change
The derivative measures how a quantity changes with respect to another.  

Example: If $s(t)$ is displacement, velocity is:  

$$
v(t) = \frac{ds}{dt}
$$

Acceleration is the derivative of velocity:  

$$
a(t) = \frac{d^2s}{dt^2}
$$

---

## 2. Maxima and Minima
- At maxima or minima, the first derivative is zero:  

$$
f'(x) = 0
$$  

- Use the **second derivative test**:  
  - If $f''(x) > 0$, local **minimum**.  
  - If $f''(x) < 0$, local **maximum**.  

---

## 3. Tangents and Normals
For curve $y=f(x)$ at point $(x_0, f(x_0))$:  
- **Slope of tangent**: $m = f'(x_0)$  
- Equation of tangent:  

$$
y - f(x_0) = f'(x_0)(x - x_0)
$$

- Equation of normal:  

$$
y - f(x_0) = -\frac{1}{f'(x_0)} (x - x_0)
$$

---

## 4. Concavity & Optimization
- If $f''(x) > 0$ → function is **convex** (bowl shaped).  
- If $f''(x) < 0$ → function is **concave** (inverted bowl).  
- Widely used in **machine learning optimization** (gradient descent).  

---

## 5. Image Gradients
For image $f(x,y)$, the gradient vector:  

$$
\nabla f(x,y) = 
\begin{bmatrix}
\frac{\partial f}{\partial x} \\
\frac{\partial f}{\partial y}
\end{bmatrix}
$$

- Direction → strongest intensity change.  
- Magnitude → rate of change (edge detection).  

---

## 6. Coding Hint (Python)
    import sympy as sp
    import numpy as np
    from scipy import ndimage
    import matplotlib.pyplot as plt

    # Example 1: Maxima/Minima
    x = sp.Symbol('x')
    f = x**3 - 6*x**2 + 9*x + 1
    f_prime = sp.diff(f, x)
    f_double = sp.diff(f, x, 2)
    crit_points = sp.solve(f_prime, x)
    print("Critical points:", crit_points)
    for cp in crit_points:
        print(cp, "-> second derivative:", f_double.subs(x, cp))

    # Example 2: Image gradient (edge detection)
    img = np.random.rand(5,5)  # dummy grayscale image
    gx = ndimage.sobel(img, axis=0)
    gy = ndimage.sobel(img, axis=1)
    grad_mag = np.hypot(gx, gy)

    plt.imshow(grad_mag, cmap='gray')
    plt.title("Gradient Magnitude")
    plt.show()

---

## 7. Do It Yourself 🚀
1. For $f(x) = x^3 - 3x^2 + 2$:  
   - Find maxima and minima using derivatives.  
   - Plot function with tangent lines at those points.  

2. Derive tangent and normal equations at point $(1, f(1))$ for $f(x) = x^2 + 2x + 3$.  

3. Use Python to compute and display image gradients of a real grayscale image.  

---

## 8. Memory Tips 🧠
- Derivative = “rate of change.”  
- Max/Min → set $f'(x)=0$, check $f''(x)$.  
- Tangent slope = derivative.  
- Image gradients = “edges = big changes.”  

---

✅ By the end of this section, you should understand:
- How derivatives describe rates of change  
- How to find maxima/minima using first & second derivatives  
- How to compute tangent and normal equations  
- How concavity relates to optimization problems  
- How gradients are used in image processing  

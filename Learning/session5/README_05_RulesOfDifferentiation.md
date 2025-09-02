# README_05_RulesOfDifferentiation

## 📌 Syllabus Coverage
This README covers the following from **Session 5 (Functions, Derivatives and Integrals)**:
- Rules of Differentiation
- Chain Rule
- Product Rule
- Properties of Differentials

---

## 1. Basic Rules

### (a) Constant Rule
If $f(x) = c$ (where $c$ is constant):  

$$
f'(x) = 0
$$

---

### (b) Identity Rule
If $f(x) = x$:  

$$
f'(x) = 1
$$

---

### (c) Power Rule
If $f(x) = x^n$ (where $n$ is a positive integer):  

$$
f'(x) = n x^{n-1}
$$

---

### (d) Constant Multiple Rule
If $f(x) = k g(x)$:  

$$
f'(x) = k g'(x)
$$

---

### (e) Sum Rule
If $f(x) = g(x) + h(x)$:  

$$
f'(x) = g'(x) + h'(x)
$$

---

## 2. Chain Rule
If $y = f(g(x))$, then:  

$$
\frac{dy}{dx} = f'(g(x)) \cdot g'(x)
$$

Example:  

$$
\frac{d}{dx} \big[(x^2 - 3x + 5)^3\big] = (6x - 9)(x^2 - 3x + 5)^2
$$

---

## 3. Product Rule
If $f(x) = g(x)h(x)$, then:  

$$
f'(x) = g'(x)h(x) + g(x)h'(x)
$$

Example:  

$$
\frac{d}{dx} \big[(x^2+1)\cos x \big] = 2x \cos x - (x^2+1)\sin x
$$

---

## 4. Properties of Differentials
For a differentiable function $F(x)$:  
1. $dF = F'(x)\, dx$  
2. $dC = 0$ (for constant $C$)  
3. $d(CF) = C \, dF$  
4. $d(u \pm v) = du \pm dv$  

---

## 5. Coding Hint (Python)
    import sympy as sp

    x = sp.Symbol('x')

    # Chain rule
    f = (x**2 - 3*x + 5)**3
    print("Chain rule:", sp.diff(f, x))

    # Product rule
    f = (x**2 + 1) * sp.cos(x)
    print("Product rule:", sp.diff(f, x))

    # Power rule
    f = x**5
    print("Power rule:", sp.diff(f, x))

---

## 6. Do It Yourself 🚀
1. Differentiate $f(x) = 7x^3 + 4x^2 - 5$.  
2. Apply product rule to $f(x) = x^2 \sin x$.  
3. Apply chain rule to $f(x) = \cos(x^2 + 1)$.  

---

## 7. Memory Tips 🧠
- Power Rule → bring exponent down, reduce by one.  
- Chain Rule → “differentiate outer, multiply inner derivative.”  
- Product Rule → “first d second + second d first.”  
- Differentials behave like algebra.  

---

✅ By the end of this section, you should understand:
- Basic rules of differentiation (constant, identity, power, sum, multiple)  
- How chain rule and product rule work  
- Properties of differentials  
- How to compute derivatives in Python  

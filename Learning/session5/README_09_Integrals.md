# README_09_Integrals

## 📌 Syllabus Coverage
This README covers the following from **Session 5 (Functions, Derivatives and Integrals)**:
- Definite and Indefinite Integrals
- Area Interpretation
- Applications of Integrals

---

## 1. Definition
An **integral** represents the accumulation of quantities, often visualized as the **area under a curve**.  

- **Indefinite integral** (antiderivative):  

$$
\int f(x) \, dx = F(x) + C
$$

where $F'(x) = f(x)$ and $C$ is the constant of integration.  

- **Definite integral** over interval $[a, b]$:  

$$
\int_a^b f(x) \, dx
$$

This gives the net area between the curve $f(x)$ and the x-axis from $x=a$ to $x=b$.  

---

## 2. Properties
- $\int (f(x) + g(x)) \, dx = \int f(x) \, dx + \int g(x) \, dx$  
- $\int k f(x) \, dx = k \int f(x) \, dx$  
- $\frac{d}{dx}\left(\int f(x) \, dx\right) = f(x)$  

(Differentiation and integration are inverse operations.)  

---

## 3. Area Interpretation
The area under a curve from $a$ to $b$ can be approximated by rectangles of width $dx$:  

$$
\text{Area} \approx \sum f(x) \cdot dx
$$

As $dx \to 0$, this becomes:  

$$
\text{Area} = \int_a^b f(x) \, dx
$$

---

## 4. Applications of Integrals
1. **Area under a curve**  
   Example: $\int_0^2 (x^2 + 1) \, dx$  

2. **Volume of solids** (by revolution)  
   Example: Volume = $\pi \int_a^b [f(x)]^2 \, dx$  

3. **Length of an arc**  
   Example: $L = \int_a^b \sqrt{1 + (f'(x))^2} \, dx$  

---

## 5. Coding Hint (Python)
    import sympy as sp

    x = sp.Symbol('x')

    # Indefinite integral
    f = x**2 + 1
    F = sp.integrate(f, x)
    print("∫(x^2 + 1) dx =", F)

    # Definite integral from 0 to 2
    result = sp.integrate(f, (x, 0, 2))
    print("∫[0,2] (x^2 + 1) dx =", result)

---

## 6. Do It Yourself 🚀
1. Compute $\int (3x^2 + 2x + 1) dx$.  
2. Find $\int_1^3 (2x) dx$ and interpret geometrically.  
3. Use Python to compute the arc length of $y = x^2$ on $[0,1]$.  

---

## 7. Memory Tips 🧠
- Integral = “sum of infinitely many small pieces.”  
- Definite integral = actual number (area).  
- Indefinite integral = family of functions (with +C).  
- Differentiation ↔ Integration are opposites.  

---

✅ By the end of this section, you should understand:
- What integrals are and their two types  
- How integrals relate to area under a curve  
- Key applications: area, volume, arc length  
- How to compute integrals by hand and in Python  

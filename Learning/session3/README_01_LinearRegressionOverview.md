# README_01_LinearRegressionOverview

## 📌 Syllabus Coverage
This README covers the following from **Session 3 (Linear Algebra Applications)**:
- Mathematical modelling of Machine Learning problem
- Linear Regression Overview
- ML problem formulation
- Explanation through an example

---

## 1. Definition
**Linear Regression** is a supervised machine learning algorithm that models the relationship between input variables (features) and an output variable (target) as a linear function.

---

## 2. Simple Linear Regression (SLR)
For one feature $X$:

$$
Y^{(i)} = \beta_0 + \beta_1 X^{(i)} + \varepsilon_i
$$

- $Y^{(i)}$: predicted value for observation $i$  
- $X^{(i)}$: input feature for observation $i$  
- $\beta_0$: intercept  
- $\beta_1$: slope (weight)  
- $\varepsilon_i$: error term  

---

## 3. Matrix Formulation of SLR
For $n$ observations:

$$
Y = X \beta + \varepsilon
$$

Where:

- $Y = \begin{bmatrix} Y^{(1)} \\ Y^{(2)} \\ \vdots \\ Y^{(n)} \end{bmatrix}$  
- $X = \begin{bmatrix} 1 & X^{(1)} \\ 1 & X^{(2)} \\ \vdots & 1 & X^{(n)} \end{bmatrix}$  
- $\beta = \begin{bmatrix} \beta_0 \\ \beta_1 \end{bmatrix}$  
- $\varepsilon = \begin{bmatrix} \varepsilon_1 \\ \varepsilon_2 \\ \vdots \\ \varepsilon_n \end{bmatrix}$  

---

## 4. Multiple Linear Regression (MLR)
For $m$ features $X_1, X_2, \dots, X_m$:

$$
Y^{(i)} = \beta_0 + \beta_1 X_1^{(i)} + \beta_2 X_2^{(i)} + \dots + \beta_m X_m^{(i)} + \varepsilon_i
$$

Matrix form:

$$
Y = X \beta + \varepsilon
$$

Where:

- $X = \begin{bmatrix}
1 & X_1^{(1)} & X_2^{(1)} & \dots & X_m^{(1)} \\
1 & X_1^{(2)} & X_2^{(2)} & \dots & X_m^{(2)} \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
1 & X_1^{(n)} & X_2^{(n)} & \dots & X_m^{(n)}
\end{bmatrix}$

- $\beta = \begin{bmatrix} \beta_0 \\ \beta_1 \\ \vdots \\ \beta_m \end{bmatrix}$  

---

## 5. Example – House Price Prediction
Predict house price ($y$) using:  
- $x_1$ = area (in 1000 sq. ft)  
- $x_2$ = number of bedrooms  

Matrix representation:

$$
Y = X \beta + \varepsilon
$$

Where:

- $Y = \begin{bmatrix} 40 \\ 55 \\ 75 \\ 85 \\ 80 \\ 70 \end{bmatrix}$  
- $X = \begin{bmatrix}
1 & 1.2 & 2 \\
1 & 1.5 & 2 \\
1 & 2.25 & 3 \\
1 & 2.5 & 3 \\
1 & 2.5 & 2 \\
1 & 1.5 & 3
\end{bmatrix}$  
- $\beta = \begin{bmatrix} \beta_0 \\ \beta_1 \\ \beta_2 \end{bmatrix}$  

---

## 6. Coding Hint (Python)
    import numpy as np

    # Input matrix (area, bedrooms)
    X = np.array([[1, 1.2, 2],
                  [1, 1.5, 2],
                  [1, 2.25, 3],
                  [1, 2.5, 3],
                  [1, 2.5, 2],
                  [1, 1.5, 3]])

    # Output vector (price)
    Y = np.array([40, 55, 75, 85, 80, 70])

    # Solve using Normal Equation: beta = (X^T X)^(-1) X^T Y
    beta = np.linalg.inv(X.T @ X) @ (X.T @ Y)
    print("Estimated coefficients (β0, β1, β2):", beta)

---

## 7. Do It Yourself 🚀
1. Derive the matrix form of SLR with 5 observations.  
2. Extend the house price model by adding a new feature: number of bathrooms.  
3. In Python, simulate data for 10 houses with 2 features and compute regression coefficients.  

---

## 8. Memory Tips 🧠
- Linear Regression = **line of best fit**.  
- Equation: $Y = X \beta + \varepsilon$ → “data as matrices.”  
- Normal Equation: $\beta = (X^TX)^{-1}X^TY$.  

---

✅ By the end of this section, you should understand:
- The basics of simple and multiple linear regression  
- How regression is written in matrix form  
- How to estimate coefficients using Python  

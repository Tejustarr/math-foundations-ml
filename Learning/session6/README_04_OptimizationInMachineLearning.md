# README_04_OptimizationInMachineLearning

## 📌 Syllabus Coverage
This README covers the following from **Session 6 (Function Optimization)**:
- Optimization in Supervised ML
- Cost and Loss Functions
- Error Minimization

---

## 1. Optimization in ML
In machine learning, the goal is to find parameters (weights) of a model that **minimize prediction error**.  

- Predictions: $\hat{y}$  
- True values: $y$  
- Error = difference between them  

Optimization finds parameters $W$ that minimize the error.  

---

## 2. Loss and Cost Functions
- **Loss Function** $L(\hat{y}, y)$ → error for a single training example.  
- **Cost Function** $J(W)$ → average of losses across the dataset.  

Example (Squared Error Loss):  

$$
L(W) = (\hat{y} - y)^2
$$  

Cost function:  

$$
J(W) = \frac{1}{n} \sum_{i=1}^n (\hat{y}^{(i)} - y^{(i)})^2
$$

---

## 3. Optimization Goal
Find  

$$
W^* = \arg \min_W J(W)
$$  

where $W^*$ are the optimal parameters.  

---

## 4. Example
For linear regression:  

$$
\hat{y} = W^T X + b
$$  

The cost function is Mean Squared Error (MSE):  

$$
J(W) = \frac{1}{n} \sum_{i=1}^n (W^T X^{(i)} + b - y^{(i)})^2
$$

---

## 5. Coding Hint (Python)
    import numpy as np

    # Example: linear regression optimization
    X = np.array([[1], [2], [3], [4]])   # feature
    y = np.array([2, 4, 6, 8])           # target

    # Initialize weight
    W = 0.0
    b = 0.0
    lr = 0.01

    # Gradient descent for few iterations
    for epoch in range(100):
        y_pred = W * X.flatten() + b
        error = y_pred - y
        cost = np.mean(error**2)

        # Gradients
        dW = np.mean(2 * X.flatten() * error)
        db = np.mean(2 * error)

        # Update
        W -= lr * dW
        b -= lr * db

    print("Optimized W:", W)
    print("Optimized b:", b)
    print("Final cost:", cost)

---

## 6. Do It Yourself 🚀
1. Write the loss function for logistic regression (cross-entropy loss).  
2. Implement a cost function for linear regression with multiple features.  
3. Use Python to simulate gradient descent on a simple quadratic function $f(x) = (x-3)^2$.  

---

## 7. Memory Tips 🧠
- **Loss = error per sample.**  
- **Cost = average error.**  
- Optimization in ML = **minimize cost.**  
- Think: “Train model = find $W$ that minimizes cost.”  

---

✅ By the end of this section, you should understand:
- Why optimization is central to ML  
- Difference between loss and cost functions  
- How error minimization is formulated  
- How to implement a simple optimization loop in Python  

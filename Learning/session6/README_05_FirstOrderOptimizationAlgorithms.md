# README_05_FirstOrderOptimizationAlgorithms

## 📌 Syllabus Coverage
This README covers the following from **Session 6 (Function Optimization)**:
- First Order Optimization Algorithms
- Gradient-based Optimization
- Pseudocode for Gradient Descent

---

## 1. What are First Order Algorithms?
- Optimization algorithms that use the **first derivative (gradient)** of the cost function to update parameters.  
- Efficient and widely used in machine learning.  
- Do **not** require higher-order derivatives (like Hessians).  

---

## 2. General Idea
- Suppose we want to minimize a cost function $J(W)$.  
- Gradient $\nabla J(W)$ gives the direction of steepest **increase**.  
- To minimize, move in the **opposite direction** of the gradient.  

Update rule:

$$
W \leftarrow W - \eta \nabla J(W)
$$

Where:  
- $W$: parameters (weights)  
- $\eta$: learning rate (step size)  

---

## 3. Gradient Descent (Pseudocode)
**Algorithm: Gradient Descent**  

1. Initialize weights $W$ randomly.  
2. Repeat until convergence:  
   a. Compute gradient $G = \nabla J(W)$.  
   b. Update weights: $W = W - \eta G$.  
3. Stop when cost function $J(W)$ stops decreasing (or after fixed iterations).  

---

## 4. Example Update
For cost function $J(W) = (W-3)^2$:  

- Derivative: $\nabla J(W) = 2(W-3)$  
- Update:  

$$
W \leftarrow W - \eta \cdot 2(W-3)
$$

If $\eta = 0.1$ and $W=0$:  
- $W \to 0 - 0.1 \cdot 2(-3) = 0.6$  

---

## 5. Coding Hint (Python)
    import numpy as np

    # Cost function J(w) = (w-3)^2
    def J(w):
        return (w - 3)**2

    # Gradient
    def grad_J(w):
        return 2*(w - 3)

    # Gradient descent
    w = 0.0
    eta = 0.1
    for epoch in range(10):
        w = w - eta * grad_J(w)
        print(f"Epoch {epoch+1}: w={w:.4f}, J(w)={J(w):.4f}")

---

## 6. Do It Yourself 🚀
1. Apply gradient descent to minimize $f(x) = x^2 + 4x + 4$.  
2. Change learning rate $\eta$ and observe:  
   - Large $\eta$ → overshoot, unstable.  
   - Small $\eta$ → very slow convergence.  
3. Implement gradient descent for a 2D function $f(x,y) = x^2 + y^2$.  

---

## 7. Memory Tips 🧠
- Gradient = slope → move **against slope** to minimize.  
- Learning rate $\eta$ controls step size.  
- Too large $\eta$ → diverge; too small $\eta$ → slow.  
- First-order methods = only gradients, no second derivatives.  

---

✅ By the end of this section, you should understand:
- What first-order optimization algorithms are  
- How gradient descent works  
- The update rule using gradients  
- How learning rate affects convergence  
- How to implement gradient descent in Python  

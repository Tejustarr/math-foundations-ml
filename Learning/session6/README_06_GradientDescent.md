# README_06_GradientDescent

## 📌 Syllabus Coverage
This README covers the following from **Session 6 (Function Optimization)**:
- Gradient Descent (detailed)
- Learning Rate
- Update Rule
- Algorithm Flow

---

## 1. Definition
**Gradient Descent** is an iterative optimization algorithm used to minimize a cost (or loss) function.  

At each step, parameters are updated in the **opposite direction** of the gradient of the cost function.

Update rule:

$$
W \leftarrow W - \eta \nabla J(W)
$$

Where:  
- $W$: parameters (weights)  
- $\nabla J(W)$: gradient of cost function  
- $\eta$: learning rate  

---

## 2. Role of Learning Rate
- **Small $\eta$** → slow convergence.  
- **Large $\eta$** → may overshoot the minimum and diverge.  
- **Adaptive $\eta$** → sometimes used to speed up convergence.  

---

## 3. Algorithm Flow
1. Initialize weights $W$ randomly.  
2. Compute cost $J(W)$.  
3. Compute gradient $\nabla J(W)$.  
4. Update weights: $W = W - \eta \nabla J(W)$.  
5. Repeat until convergence or max iterations.  

Flow chart summary:  

- Start → Initialize $W$ → Compute gradient → Update weights → Check stop criteria → End  

---

## 4. Visualization
- Gradient descent can be visualized as “rolling downhill” on the cost function curve.  
- For convex cost functions → converges to global minimum.  
- For non-convex cost functions → may get stuck in local minima.  

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
    history = []
    for epoch in range(20):
        w = w - eta * grad_J(w)
        history.append((w, J(w)))
        print(f"Epoch {epoch+1}: w={w:.4f}, J(w)={J(w):.4f}")

    # Final result
    print("Optimal w:", w)

---

## 6. Do It Yourself 🚀
1. Run gradient descent with $\eta=0.01$, $\eta=0.1$, and $\eta=1$ for $f(x) = (x-3)^2$.  
   - Compare convergence speed and stability.  
2. Extend gradient descent to $f(x,y) = x^2 + y^2$.  
   - Update rule:  
     $$
     x \leftarrow x - \eta \frac{\partial f}{\partial x}, \quad
     y \leftarrow y - \eta \frac{\partial f}{\partial y}
     $$  
3. Implement a stopping condition based on tolerance: stop if $|J(W)_{t} - J(W)_{t-1}| < \epsilon$.  

---

## 7. Memory Tips 🧠
- Gradient descent = “roll downhill.”  
- Learning rate = step size.  
- Convex cost → guaranteed global min.  
- Non-convex cost → possible local mins.  

---

✅ By the end of this section, you should understand:
- How gradient descent works in detail  
- The role of learning rate in optimization  
- Algorithm flow and stopping conditions  
- How to implement and visualize gradient descent in Python  

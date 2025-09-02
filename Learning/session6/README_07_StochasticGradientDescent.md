# README_07_StochasticGradientDescent

## 📌 Syllabus Coverage (Bonus)
This README extends **Session 6 (Function Optimization)** to include:
- Stochastic Gradient Descent (SGD)

---

## 1. Definition
**Stochastic Gradient Descent (SGD)** is a variant of gradient descent where parameter updates are made using **a single training example (or a small batch)** instead of the entire dataset.  

This introduces randomness (“stochasticity”), which makes updates noisier but faster.  

---

## 2. Update Rule
For a dataset with $n$ samples:  

- Standard Gradient Descent (Batch GD):  

$$
W \leftarrow W - \eta \nabla J(W)
$$

- Stochastic Gradient Descent (SGD):  

$$
W \leftarrow W - \eta \nabla L(W; x^{(i)}, y^{(i)})
$$  

where $L$ is the loss for a **single sample** $(x^{(i)}, y^{(i)})$.  

- Mini-Batch Gradient Descent: use a small subset (batch) instead of one sample.  

---

## 3. Comparison: GD vs SGD
- **Gradient Descent (GD)**:  
  - Uses all data to compute gradient.  
  - Stable convergence but computationally expensive.  

- **SGD**:  
  - Uses one sample at a time.  
  - Faster updates, handles large datasets.  
  - Path to minimum is noisy but often avoids local minima.  

---

## 4. Coding Hint (Python)
    import numpy as np

    # Example: SGD for linear regression (y = Wx + b)
    X = np.array([[1], [2], [3], [4]])   # feature
    y = np.array([2, 4, 6, 8])           # target

    W, b = 0.0, 0.0
    lr = 0.01
    epochs = 20

    for epoch in range(epochs):
        for i in range(len(X)):
            xi, yi = X[i], y[i]
            y_pred = W*xi + b
            error = y_pred - yi

            # Gradients (based on one sample)
            dW = 2 * xi * error
            db = 2 * error

            # Update
            W -= lr * dW
            b -= lr * db

        print(f"Epoch {epoch+1}: W={W:.4f}, b={b:.4f}")

---

## 5. Do It Yourself 🚀
1. Implement mini-batch gradient descent for batch size = 2.  
2. Compare convergence of Batch GD vs SGD on the same dataset.  
3. Plot cost vs epochs for both methods and observe differences.  

---

## 6. Memory Tips 🧠
- GD = **whole dataset** → stable, slow.  
- SGD = **one sample** → noisy, fast.  
- Mini-batch = compromise between speed and stability.  
- Noise in SGD can help escape local minima.  

---

✅ By the end of this section, you should understand:
- What Stochastic Gradient Descent is  
- How it differs from batch gradient descent  
- Why SGD is widely used in ML training  
- How to implement SGD in Python  

# 📘 Session 1 — Linear Algebra Overview

This file introduces **Linear Algebra**, its scope, and why it is fundamental in Data Science & Machine Learning.

---

## 🔹 1. What is Linear Algebra?

* **Definition:** Linear algebra studies vectors, matrices, and linear transformations between vector spaces.
* It provides a compact language for solving systems of linear equations, representing data, and performing transformations.

**In short:** Linear algebra = math of vectors and matrices.

---

## 🔹 2. Why is Linear Algebra Important?

* Core foundation for modern applied mathematics.
* Used in **machine learning, deep learning, computer vision, NLP, recommendation systems, scientific computing**.
* Enables efficient representation & manipulation of large datasets.

---

## 🔹 3. Applications in Data Science / ML

### a) Machine Learning Formulation

* Most ML problems reduce to matrix equations:
  $y = X\beta + \epsilon$
* Example: linear regression uses matrix form to solve for parameters efficiently.

### b) Natural Language Processing (NLP)

* Words and documents represented as high-dimensional vectors.
* Example: Bag of Words (BoW), TF–IDF, Word Embeddings.

### c) Images

* An image = matrix of pixel values.
* Linear algebra enables filtering, compression, transformations.

### d) Recommendation Systems

* User–item ratings stored as matrices.
* Matrix factorization (SVD, PCA) → latent factors → predict missing ratings.

### e) Medical / Business Data

* Patient record = feature vector.
* Market basket analysis = transaction matrix.

---

## 🔹 4. Linear Equations & Matrix Form

* Linear system example:

  $$
  2a + 3b + 4c = 11 \\
  3a + 5b + 5c = 15 \\
  5a + 6b + 3c = 19
  $$

* Matrix representation:

  $$
  A x = b
  $$

where A = coefficient matrix, x = variables vector, b = result vector.

---

## 🔹 5. Python Hints

```python
import numpy as np

# Example: system Ax = b
A = np.array([[2,3,4],[3,5,5],[5,6,3]])
b = np.array([11,15,19])

x = np.linalg.solve(A,b)
print(x)  # solution vector [a, b, c]
```

---

## ✅ Quick Recap

* Linear Algebra = study of vectors, matrices, linear transformations.
* Applications: ML models, NLP, image processing, recommender systems.
* Linear systems can be expressed as compact matrix equations.
* Python’s `numpy.linalg` helps solve them directly.

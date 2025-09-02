# README_02_ApplicationsOfLinearAlgebra

## 📌 Syllabus Coverage
This README covers the following from **Session 1 (Introduction to Linear Algebra)**:
- Applications of Linear Algebra

---

## 1. Definition
Applications of Linear Algebra refer to how vectors, matrices, and linear transformations are used to model and solve real-world problems in mathematics, computer science, and data science.

Linear Algebra provides a **framework to represent and manipulate data** in compact and efficient forms.

---

## 2. Common Applications
1. **Formulation of Machine Learning Problems**  
   - Linear Regression and classification can be expressed in terms of matrices.  
   - Example: Predicting $Y$ from $X$ can be written as $Y = XW + b$.

2. **Image Processing**  
   - Images are represented as matrices of pixel values.  
   - Linear transformations (rotation, scaling) and filters are matrix operations.

3. **Dimensionality Reduction**  
   - Large datasets can be simplified using techniques like PCA (Principal Component Analysis).  
   - PCA relies on eigenvectors and eigenvalues from linear algebra.

4. **Natural Language Processing (NLP)**  
   - Words/documents can be represented as vectors.  
   - Word count vectors and embeddings are linear algebra structures.

5. **Recommendation Systems**  
   - User–item interactions are stored in matrices.  
   - Matrix factorization is used to predict missing values.

6. **Computer Vision**  
   - Object detection and transformations of images use matrix operations.  

---

## 3. Mathematical Representation
- **Linear Transformation in ML models**:

  $$
  Y = XW + b
  $$

  Where:  
  - $X$: Input feature matrix  
  - $W$: Weight matrix  
  - $b$: Bias vector  
  - $Y$: Predictions  

- **Image as Matrix**:

  A grayscale image = matrix of intensity values.  
  A color image (RGB) = 3 matrices stacked (Red, Green, Blue channels).

---

## 4. Coding Hint (Python)
    import numpy as np

    # Example: Linear transformation
    X = np.array([[1, 2],
                  [3, 4],
                  [5, 6]])   # Feature matrix

    W = np.array([[2],
                  [1]])      # Weights

    b = 1                   # Bias

    # Compute prediction Y = XW + b
    Y = X @ W + b
    print("Predictions:\n", Y)

    # Example: Image as matrix
    image = np.random.randint(0, 256, (4, 4))  # 4x4 grayscale image
    print("Image matrix:\n", image)

---

## 5. Do It Yourself 🚀
1. Represent a $3 \times 3$ grayscale image using a NumPy array.  
   - Multiply it by a scalar (e.g., 2) to brighten the image.  

2. Given a feature matrix $X$ (4 samples × 2 features), create a random weight vector $W$ and compute $Y = XW$.  

3. Write down in words how PCA (dimensionality reduction) uses eigenvectors.  

---

## 6. Memory Tips 🧠
- **Data → Matrix → Operation → Result**.  
- Always think: “If it’s big data, it’s in a matrix.”  
- ML pipeline: **Input (X) → Linear Transformation (W, b) → Output (Y)**.  

---

✅ By the end of this section, you should understand:
- How Linear Algebra is applied in ML and DS  
- How images, text, and data are represented in matrices  
- How to perform a simple linear transformation in Python  

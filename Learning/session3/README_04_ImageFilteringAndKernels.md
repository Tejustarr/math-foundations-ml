# README_04_ImageFilteringAndKernels

## 📌 Syllabus Coverage
This README covers the following from **Session 3 (Linear Algebra Applications)**:
- Image Filtering
- Kernels (Convolution)
- Applications: sharpening, blurring, edge detection, feature extraction

---

## 1. Definition
**Filtering** in image processing modifies pixel intensities using a mathematical operation.  
It is often implemented through **convolution with a kernel (filter matrix)**.  

---

## 2. Convolution Operation
A kernel (or mask) $W$ slides over the image $I$.  
For each pixel, multiply the overlapping values and sum them:  

$$
I'(x,y) = \sum_{i=-k}^{k} \sum_{j=-k}^{j} W(i,j) \cdot I(x+i, y+j)
$$

- $I(x,y)$ = original image pixel  
- $W$ = kernel weights  
- $I'(x,y)$ = filtered image pixel  

---

## 3. Common Kernels

1. **Identity Kernel** (no change)  

$$
\begin{bmatrix}
0 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 0
\end{bmatrix}
$$

---

2. **Sharpening Kernel**  

$$
\begin{bmatrix}
0 & -1 & 0 \\
-1 & 5 & -1 \\
0 & -1 & 0
\end{bmatrix}
$$

---

3. **Edge Detection Kernel**  

$$
\begin{bmatrix}
-1 & -1 & -1 \\
-1 & 8 & -1 \\
-1 & -1 & -1
\end{bmatrix}
$$

---

4. **Blurring Kernel (Average Filter)**  

$$
\frac{1}{9} \begin{bmatrix}
1 & 1 & 1 \\
1 & 1 & 1 \\
1 & 1 & 1
\end{bmatrix}
$$

---

## 4. Coding Hint (Python)
    import numpy as np
    from scipy.signal import convolve2d
    import matplotlib.pyplot as plt
    from skimage import data, color

    # Example image (grayscale)
    img = color.rgb2gray(data.astronaut())

    # Define a blur kernel
    kernel = np.ones((3,3)) / 9.0

    # Apply convolution
    filtered = convolve2d(img, kernel, mode='same', boundary='symm')

    # Display results
    plt.subplot(1,2,1)
    plt.title("Original")
    plt.imshow(img, cmap='gray')

    plt.subplot(1,2,2)
    plt.title("Blurred")
    plt.imshow(filtered, cmap='gray')
    plt.show()

---

## 5. Do It Yourself 🚀
1. Apply an edge detection kernel to a grayscale image and visualize the result.  
2. Create your own $3 \times 3$ kernel and test how it modifies the image.  
3. Verify that using a kernel with fractions (like $\tfrac{1}{16}$ weights) produces a smoother blur.  

---

## 6. Memory Tips 🧠
- **Kernel = small matrix filter.**  
- **Convolution = multiply + sum.**  
- Sharpen → highlights details.  
- Blur → smooths details.  
- Edge detect → highlights boundaries.  

---

✅ By the end of this section, you should understand:
- What kernels and convolution are in image processing  
- Different types of kernels and their effects  
- How to apply filters in Python for sharpening, blurring, and edge detection  

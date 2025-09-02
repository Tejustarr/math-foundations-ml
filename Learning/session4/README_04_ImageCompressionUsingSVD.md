# README_04_ImageCompressionUsingSVD

## 📌 Syllabus Coverage
This README covers the following from **Session 4 (Linear Algebra Applications – PCA & SVD)**:
- Image Compression using SVD

---

## 1. Idea
- Images can be represented as matrices of pixel values.  
- **SVD** allows factorization of an image matrix into $U \Sigma V^T$.  
- By keeping only the **top $k$ singular values**, we can approximate the original image with much less storage.  

---

## 2. Mathematical Formulation
Given an image matrix $A$ (size $m \times n$):  

$$
A = U \Sigma V^T
$$

Approximation using top $k$ singular values:  

$$
A_k = U_k \Sigma_k V_k^T
$$

Where:  
- $U_k$: first $k$ columns of $U$  
- $\Sigma_k$: first $k$ singular values (diagonal matrix)  
- $V_k$: first $k$ columns of $V$  

---

## 3. Compression
- Original storage = $m \times n$ values.  
- Compressed storage = $mk + k + nk = k(m+n+1)$ values.  
- For small $k \ll \min(m,n)$, compression is significant.  

---

## 4. Coding Hint (Python)
    import numpy as np
    import matplotlib.pyplot as plt
    from skimage import color, data

    # Example grayscale image
    img = color.rgb2gray(data.astronaut())
    m, n = img.shape

    # Compute SVD
    U, S, Vt = np.linalg.svd(img, full_matrices=False)

    # Reconstruct image using top k singular values
    def svd_compress(k):
        Uk = U[:, :k]
        Sk = np.diag(S[:k])
        Vk = Vt[:k, :]
        return Uk @ Sk @ Vk

    # Compare original vs compressed
    ks = [5, 20, 100]
    plt.figure(figsize=(10,4))

    plt.subplot(1,4,1)
    plt.title("Original")
    plt.imshow(img, cmap='gray')

    for i, k in enumerate(ks, start=2):
        plt.subplot(1,4,i)
        plt.title(f"k={k}")
        plt.imshow(svd_compress(k), cmap='gray')

    plt.show()

---

## 5. Do It Yourself 🚀
1. Load a grayscale image and compress it using $k = 10, 50, 100$. Compare results.  
2. Calculate storage savings for each $k$ using the formula $k(m+n+1)$.  
3. Try compressing an RGB image by applying SVD separately on R, G, and B channels.  

---

## 6. Memory Tips 🧠
- Large singular values capture **most important features** of the image.  
- Small singular values capture **fine details/noise**.  
- More $k$ → better quality, less compression.  
- Fewer $k$ → more compression, some loss of detail.  

---

✅ By the end of this section, you should understand:
- How SVD is used for image compression  
- The trade-off between compression ratio and image quality  
- How to implement image compression using SVD in Python  

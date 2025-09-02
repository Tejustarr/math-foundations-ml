# README_02_ImageBasicsAndPixels

## 📌 Syllabus Coverage
This README covers the following from **Session 3 (Linear Algebra Applications)**:
- Image basics: Pixel and representation
- Digitization
- Channels (Grayscale, RGB)
- Intensity vs Spatial domain

---

## 1. What is an Image?
An image is a **2D function** $P(x,y)$ where $x,y$ are spatial coordinates and $P(x,y)$ represents the **intensity (brightness or color value)** at that point.  

In digital form, images are stored as **matrices of pixels**.  

---

## 2. Pixels
- **Pixel = picture element**, the smallest unit of a digital image.  
- Stored as integer values (commonly in range $0 \text{ to } 255$ for 8-bit images).  
  - $0$ → black  
  - $255$ → white  
- Each pixel corresponds to a **single square point** in the image.  

---

## 3. Digitization
Converting continuous real-world images into digital form involves:  
1. **Sampling** – selecting pixel locations on a 2D grid.  
2. **Quantization** – mapping intensity values into discrete levels (e.g., $0-255$).  

---

## 4. Image Representation
- Grayscale Image: each pixel has **one value** (intensity).  
- Color Image (RGB): each pixel is a **3-element vector**:  

$$
\text{Pixel} = [R, G, B]
$$

Example:  
- $(R,G,B) = (255,255,255)$ → white  
- $(R,G,B) = (0,0,0)$ → black  
- Other combinations → different colors.  

---

## 5. Channels
- **Grayscale** → 1 channel (intensity).  
- **RGB** → 3 channels:  
  - Red (R)  
  - Green (G)  
  - Blue (B)  

Image as 3D array:  

$$
\text{Image Shape} = (H, W, C)
$$  

- $H$: height (rows of pixels)  
- $W$: width (columns of pixels)  
- $C$: channels (1 for grayscale, 3 for RGB)  

---

## 6. Coding Hint (Python)
    import numpy as np
    from skimage import io
    import matplotlib.pyplot as plt

    # Load an image
    img = io.imread('sample_image.png')

    print("Image shape:", img.shape)   # (Height, Width, Channels)
    print("Pixel at (0,0):", img[0,0]) # RGB values

    # Convert to grayscale
    from skimage.color import rgb2gray
    gray = rgb2gray(img)
    print("Grayscale shape:", gray.shape)

    # Show images
    plt.subplot(1,2,1)
    plt.title("Original RGB")
    plt.imshow(img)

    plt.subplot(1,2,2)
    plt.title("Grayscale")
    plt.imshow(gray, cmap='gray')
    plt.show()

---

## 7. Do It Yourself 🚀
1. Represent a $4 \times 4$ grayscale image as a NumPy array with values in $[0,255]$.  
2. Create a $2 \times 2$ RGB image (manually assign values for each pixel).  
3. Write Python code to split an RGB image into R, G, and B channels separately.  

---

## 8. Memory Tips 🧠
- **Pixel = atomic element of image.**  
- **Grayscale = 1 number per pixel, RGB = 3 numbers per pixel.**  
- Image = **matrix of pixels**, each entry = intensity or color vector.  

---

✅ By the end of this section, you should understand:
- What pixels are and how images are represented  
- The difference between grayscale and RGB channels  
- How digitization (sampling + quantization) works  
- How to handle image arrays in Python  

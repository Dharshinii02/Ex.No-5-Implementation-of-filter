# Ex.No-5-Implementation-of-filter


**Developed By:** Dharshini J  
**Register Number:** 212224240036
**Title:** Ex.No: 5 – Implementation of Filters


## Aim
To implement different image filtering techniques using OpenCV and Python to smooth images, reduce noise, and detect edges.

## Software Used
- Python
- OpenCV
- NumPy
- Matplotlib
- Jupyter Notebook

## Algorithm
1. Import the required libraries: OpenCV, NumPy, and Matplotlib.
2. Read the input image using `cv2.imread()`.
3. Convert the image from BGR to RGB format.
4. Apply the Average Filter using a kernel.
5. Apply the Weighted Average Filter to smooth the image.
6. Apply Gaussian Blur to reduce image noise.
7. Apply Median Blur to remove noise while preserving edges.
8. Apply the Laplacian Kernel to highlight image details.
9. Apply the Laplacian Operator for edge detection.
10. Display the original and filtered images using Matplotlib.

## Program

### 1. Average Filter

```python
import cv2
import matplotlib.pyplot as plt
import numpy as np

image1 = cv2.imread("pariss.jpg")
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

kernel = np.ones((11,11), np.float32) / 169
image3 = cv2.filter2D(image2, -1, kernel)

plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")

plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```

### 2. Weighted Average Filter

```python
kernel1 = np.array([[1,2,1],
                    [2,4,2],
                    [1,2,1]]) / 16

image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)
image3 = cv2.filter2D(image2, -1, kernel1)

plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")

plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```

### 3. Gaussian Blur

```python
gaussian_blur = cv2.GaussianBlur(image2, (33,33), 0, 0)

plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")

plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

### 4. Median Blur

```python
median = cv2.medianBlur(image2, 13)

plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")

plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

### 5. Laplacian Kernel

```python
kernel2 = np.array([[-1,-1,-1],
                    [2,-2,1],
                    [2,1,-1]])

image3 = cv2.filter2D(image2, -1, kernel2)

plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")

plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```

### 6. Laplacian Operator

```python
laplacian = cv2.Laplacian(image2, cv2.CV_64F)

plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")

plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## Output

The following outputs are obtained:

### i) Display the Original Image and Average Filter Image

<img width="747" height="260" alt="image" src="https://github.com/user-attachments/assets/fa8c136b-5a62-47fa-bba7-529010e71755" />

### ii) Display the Original Image and Weighted Average Filter Image

<img width="535" height="200" alt="image" src="https://github.com/user-attachments/assets/4cc71356-7b13-4dcd-a65c-010fbf84b94f" />


### iii) Display the Original Image and Gaussian Blur Image

<img width="537" height="213" alt="image" src="https://github.com/user-attachments/assets/9ba2d3a8-911b-4221-bb15-23fb654cf871" />

### iv) Display the Original Image and Median Blur Image

<img width="750" height="256" alt="image" src="https://github.com/user-attachments/assets/c50467b0-9f69-44a1-bf02-1d6db6577eae" />


### v) Display the Original Image and Laplacian Kernel Image

<img width="548" height="190" alt="image" src="https://github.com/user-attachments/assets/1ce0f512-a253-4a94-925f-6a2832f62b6d" />


### vi) Display the Original Image and Laplacian Operator Image

<img width="523" height="192" alt="image" src="https://github.com/user-attachments/assets/445e3f75-9c08-4a57-8c07-46a723377ee3" />


## Result

Thus, different image filtering techniques, including Average Filter, Weighted Average Filter, Gaussian Blur, Median Blur, Laplacian Kernel, and Laplacian Operator, were successfully implemented using OpenCV and Python.

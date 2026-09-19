# Workshop3 - Canny Edge Detection

## Aim
To perform edge detection on a given image using the Canny Edge Detection algorithm in OpenCV.

## Software Required
Python 3.x
OpenCV (cv2 module)
NumPy
Matplotlib

## Algorithm (5 Steps)
Step 1: Read and Convert Image: Load the image and convert it to grayscale for processing.
Step 2: Noise Reduction: Apply Gaussian Blur to smooth the image and reduce noise.
Step 3: Compute Gradients: Detect intensity gradients using Sobel filters internally.
Step 4: Non-Max Suppression: Thin the detected edges to preserve sharp boundaries.
Step 5: Thresholding and Hysteresis: Apply double threshold to identify and connect strong edges.

## Program:
#### NAME: Meyyappan T
#### REG.NO: 212223240086

```
import cv2
import matplotlib.pyplot as plt

img = cv2.imread('image_01.png',cv2.IMREAD_GRAYSCALE)

blurred =cv2.GaussianBlur(img, (5,5),0)

edges = cv2.Canny(blurred, 50, 150)

plt.figure(figsize=(10,5))
plt.subplot(121),plt.imshow(img, cmap='gray')
plt.title('Original Image'), plt.axis('off')
plt.subplot(122),plt.imshow(edges, cmap='gray')
plt.title('Detected Edges'), plt.axis('off')
plt.show()
```

<img width="1095" height="377" alt="image" src="https://github.com/user-attachments/assets/edb828ad-4050-41a7-a843-6250dc878914" />



## Result
The Canny Edge Detection algorithm successfully detects and highlights the edges of objects in the input image, providing a clear edge map of the scene.

# Exp-6--Record-EDGE-DETECTION
Edge-detection-opencv
Aim
To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

Software Required
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib
⚙️ Algorithm
Step 1:
Import all the necessary modules for the program.

Step 2:
Load an image using cv2.imread().

Step 3:
Convert the image to grayscale.

Step 4:
Apply Sobel operator using OpenCV to detect edges.

Step 5:
Apply Prewitt operator using custom kernels.

Step 6:
Apply Roberts operator using custom kernels.

Step 7:
Apply Laplacian operator using OpenCV.

Step 8:
Apply Canny edge detector using OpenCV.

Step 9:
Display all edge-detected images for comparison.

Developed By
Name: Deepika V
Register No: 212224240030

PROGRAM:

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('myimage.png')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)
sobel_combined = cv2.magnitude(sobel_x, sobel_y)

plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')

laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)

plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')

canny_edges = cv2.Canny(gray_image, 50, 150)

plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')

```

Output

<img width="279" height="415" alt="image" src="https://github.com/user-attachments/assets/431ae356-ba22-4e5e-9383-c85023bddec5" />

<img width="268" height="412" alt="image" src="https://github.com/user-attachments/assets/648c1f18-0a80-404d-b14d-b1a2db01e7ae" />

<img width="296" height="417" alt="image" src="https://github.com/user-attachments/assets/9383b949-3a53-482d-b9dd-eda0d6b02c31" />

<img width="270" height="403" alt="image" src="https://github.com/user-attachments/assets/bea5f0a6-33e2-48b6-a48f-4643277ed70f" />

Result

Thus, edges are successfully detected using Sobel, Prewitt, Roberts, Laplacian, and Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.

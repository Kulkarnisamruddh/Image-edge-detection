# Image-edge-detection
What is an edge detection in computer vision -
It is an image processing technique for identifying and locating the boundaries or edges of objects in an image. It is used to identify and detect the discontinuities in the image intensity and extract the outlines of objects present in an image.
#----here is an example code for edge detection
Simple image detection using dog photo-
![download](https://github.com/user-attachments/assets/80e06096-ad5c-4afd-93e3-b94705863485)

import cv2
import matplotlib.pyplot as plt

img = cv2.imread('download.jpg')
if img is None:
    raise ValueError("Image not found")

gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

edges = cv2.Canny(gray, 50, 150, apertureSize=3, L2gradient=True)

plt.figure()
plt.title('Spider Edges')
plt.imshow(edges, cmap='gray')
plt.axis('off')
plt.show()

cv2.imwrite('dancing-spider-canny.png', edges)
<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/dbc6f89e-135c-40b0-91b3-03ce7fd0535e" />

 


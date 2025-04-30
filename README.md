# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

Step1:
Import necessary libraries such as OpenCV, NumPy, and Matplotlib for image processing and visualization.

Step2:
Read the input image using cv2.imread() and store it in a variable for further processing

Step3:
Apply various transformations like translation, scaling, shearing, reflection, rotation, and cropping by defining corresponding functions:

1.Translation moves the image along the x or y-axis. 2.Scaling resizes the image by scaling factors. 3.Shearing distorts the image along one axis. 4.Reflection flips the image horizontally or vertically. 5.Rotation rotates the image by a given angle.

Step4:
Display the transformed images using Matplotlib for visualization. Convert the BGR image to RGB format to ensure proper color representation.

## Program:
```python
Developed By: Thamizh Kumaran S
Register Number:212223240166
```
```
i)Original Image:

import cv2
import matplotlib.pyplot as plt
import numpy as np
image = cv2.imread('Imagehd.jpg')
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB)) 
plt.title("Original Image")  
plt.axis('off')

ii)Image Translation:

tx, ty = 200, 100
M_translation = np.float32([[1, 0, tx], [0, 1, ty]])
translated_image = cv2.warpAffine(image, M_translation, (image.shape[1], image.shape[0]))
plt.imshow(cv2.cvtColor(translated_image, cv2.COLOR_BGR2RGB))  # Display the translated image
plt.title("Translated Image")  
plt.axis('off')

iii) Image Scaling:

fx, fy = 1.0, 3.0 
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)
plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB))  
plt.title("Scaled Image")  # Set title
plt.axis('off')

iv)Image shearing:

shear_matrix = np.float32([[1, -0.5, 0], [-0.5, 1, 0]])
sheared_image = cv2.warpAffine(image, shear_matrix, (image.shape[1], image.shape[0]))
plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB)) 
plt.title("Sheared Image")  
plt.axis('off')

v)Image Reflection:

reflected_image = cv2.flip(image, 2)
plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB)) 
plt.title("Reflected Image") 
plt.axis('off')

vi)Image Rotation:

image = cv2.imread('Imagehd.jpg')
(h, w) = image.shape[:2]
M = cv2.getRotationMatrix2D((w // 2, h // 2), 45, 1)
rotated_image = cv2.warpAffine(image, M, (w, h))
plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB))
plt.title("Rotated Image")
plt.axis('off')

vii)Image Cropping:

x, y, w, h = 150, 150, 300, 100
cropped_image = image[y:y+h, x:x+w]
plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB))
plt.title("Cropped Image") 
plt.axis('off')

```
## Output:

### i)Original Image:

![download](https://github.com/user-attachments/assets/3fbdd85a-3411-4c73-97c7-4406a878409d)



### ii)Image Translation

![download 2](https://github.com/user-attachments/assets/a279cb9c-9e63-461e-bb20-c0f698d8b03b)


### iii) Image Scaling

![download 3](https://github.com/user-attachments/assets/9af4aa11-b14a-4306-8297-54c52e9d8bab)



### iv)Image shearing

![download 4](https://github.com/user-attachments/assets/7fd4855d-47c5-41df-9b4b-d17dbc39a2cc)



### v)Image Reflection

![download 5](https://github.com/user-attachments/assets/d1788d54-e3e3-48e3-b554-1cfd43217a86)



### vi)Image Rotation

![download 6](https://github.com/user-attachments/assets/575f0ef5-51f2-445f-bbc2-16243321ca09)



### vii)Image Cropping

![download 7](https://github.com/user-attachments/assets/5e687ae6-9f1a-4271-9957-519aa2507bf9)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.

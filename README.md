# IMPLEMENTATION_OF_EROSION_AND_DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
##### 1.Anaconda - Python 3.7
##### 2.OpenCV

## Algorithm:
### Step1:
Import required libraries (OpenCV, NumPy) and load the image in grayscale

### Step2:
Define a structuring element (kernel) for morphological operations.

### Step3:
Apply erosion using cv2.erode() on the image with the defined kernel.

### Step4:
Apply dilation using cv2.dilate() on the image with the same kernel.

### Step5:
Display and compare the original, eroded, and dilated images.

## Program
```
Developed by:VEDHANTH H
Reg NO: 212224240181
```
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'HASINI', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
```
kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
```
```
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')
```
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Dilated Image")
plt.axis('off')
```
## Output:

### Display the input Image
<img width="756" height="534" alt="image" src="https://github.com/user-attachments/assets/3b5d2604-59c6-44dc-a8cc-3d4779db10f3" />


### Display the Eroded Image
<img width="862" height="548" alt="image" src="https://github.com/user-attachments/assets/bd30b33c-0d86-4aad-9734-d0366528949e" />


### Display the Dilated Image
<img width="710" height="533" alt="image" src="https://github.com/user-attachments/assets/4235211c-9111-46d3-9040-d75a2af48612" />



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.

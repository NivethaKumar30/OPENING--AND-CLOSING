# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the Text using cv2.putText
### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

 
## Program and Output:

### Import the necessary packages
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

### Read and display the original image
```p
image = cv2.imread("fp.jpg")
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.figure(figsize=(8, 4))
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```
![image](https://github.com/user-attachments/assets/8da7b1f9-2657-4367-b689-3c47d0d3e9f6)

### Create the structuring element
```p
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
```

### Use Opening operation
```p
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
plt.figure(figsize=(8, 4))
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```
![image](https://github.com/user-attachments/assets/c7f91102-61c3-4976-8c38-c1d97fcdb86d)

### Use Closing Operation
```p
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
plt.figure(figsize=(8, 4))
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")
```
![image](https://github.com/user-attachments/assets/03cb10a8-05ce-4955-b8ec-b32ce74f25b4)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.

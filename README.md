# EDGE--LINKING-HOUGH-TRANSFORM
## Aim:
To write a Python program to detect the lines using Hough Transform.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>


## Program:
```
Developer name:Pooja A
Register no:212222240072
```
```
# Read image and convert it to grayscale image:

import numpy as np
import matplotlib.pyplot as plt
import cv2
image = cv2.imread("carss.jpg",0)
img = cv2.GaussianBlur(image,(3,3),0)
plt.axis('off')
plt.imshow(img)
plt.show()
```



# Find the edges in the image using canny detector and display



# Detect points that form a line using HoughLinesP



# Draw lines on the image



# Display the result




```
## Output

### Input image and grayscale image
<br>
<br>
<br>
<br>

### Canny Edge detector output
<br>
<br>
<br>
<br>


### Display the result of Hough transform
<br>
<br>
<br>
<br>



## Result:
Thus the program is written with python and OpenCV to detect lines using Hough transform. 

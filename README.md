# Ex-08-Edge-Linking-using-Hough-Transform
## Aim:
To write a Python program to detect the lines using Hough Transform.

## Software Required:
Anaconda - Python 3.7 .

## Algorithm:
### Step 1:
Import all the necessary packages required for the program.

### Step 2:
Load a image using imread() from cv2 module.

### Step 3:
Convert the image to grayscale image.

### Step 4:
Using Canny edge operator from cv2, detect the edges of the image.

### Step 5:
Using the HoughLinesP(), detect the line co-ordinates for every points in the images. Using For loop, draw the lines on the found co-ordinates.

### Step 6:
Display the image found by the HoughLinesP() and end the program.

## Program:
```
Developed By :Pooja A
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
```
# Find the edges in the image using canny detector and display:

edge = cv2.Canny(img,50,100)
plt.imshow(edge,cmap='gray')
plt.title('Edged Image after applying Canny Edge Detector')
plt.xticks([])
plt.yticks([])
plt.show()
```
```
# Detect points that form a line using HoughLinesP:

lines=cv2.HoughLinesP(edge,1,np.pi/180, threshold=80, minLineLength=50,maxLineGap=250)
```
```
# Draw lines on the image:

for line in lines:
    x1,y1,x2,y2 = line[0]
    cv2.line(edge,(x1,y1),(x2,y2),(250,0,0),3)
```
```
# Display the result:

plt.imshow(edge)
plt.axis('off')
plt.show()
```

## Output:
### Input image:


### Grayscale image:
Di8 1

### Canny Edge detector output:
Di8 2

### Display the result of Hough transform:
Di8 3

## Result:
Thus the program is written with python and OpenCV to detect lines using Hough transform.

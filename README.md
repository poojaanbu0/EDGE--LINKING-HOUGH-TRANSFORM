# Edge-Linking-using-Hough-Transform
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
Developed By : Pooja A
Register no:212222240072
```

# Read image and convert it to grayscale image:
```python
import numpy as np
import matplotlib.pyplot as plt
import cv2
image = cv2.imread("road.jpg",0)
img = cv2.GaussianBlur(image,(3,3),0)
plt.axis('off')
plt.imshow(img)
plt.show()
```

# Find the edges in the image using canny detector and display:
```python
edge = cv2.Canny(img,50,100)
plt.imshow(edge,cmap='gray')
plt.title('Canny Edge Detector')
plt.xticks([])
plt.yticks([])
plt.show()
```

# Detect points that form a line using HoughLinesP:
```python
lines=cv2.HoughLinesP(edge,1,np.pi/180, threshold=80, minLineLength=50,maxLineGap=250)
```

# Draw lines on the image:
```python
for line in lines:
    x1,y1,x2,y2 = line[0]
    cv2.line(edge,(x1,y1),(x2,y2),(250,0,0),3)
```

# Display the result:
```python
plt.imshow(edge)
plt.axis('off')
plt.show()
```

## Output:
### Input image:
![WhatsApp Image 2023-11-14 at 01 26 49_0cd65e7e](https://github.com/poojaanbu0/EDGE--LINKING-HOUGH-TRANSFORM/assets/119390329/2a4682ba-2d34-4a6b-827d-e9d83e899c62)

### Grayscale image:
![WhatsApp Image 2023-11-14 at 01 28 57_5454e417](https://github.com/poojaanbu0/EDGE--LINKING-HOUGH-TRANSFORM/assets/119390329/800ddcf3-6cbc-4465-a453-e4d598fd106e)

### Canny Edge detector output:
![WhatsApp Image 2023-11-14 at 01 29 36_87074133](https://github.com/poojaanbu0/EDGE--LINKING-HOUGH-TRANSFORM/assets/119390329/e38f11a4-4c78-4150-913d-1899493fda41)

### Display the result of Hough transform:
![WhatsApp Image 2023-11-14 at 01 30 11_d048d011](https://github.com/poojaanbu0/EDGE--LINKING-HOUGH-TRANSFORM/assets/119390329/e27f7aa4-1ae0-4bad-a270-761fd520fa56)

## Result:
Thus the program is written with python and OpenCV to detect lines using Hough transform.

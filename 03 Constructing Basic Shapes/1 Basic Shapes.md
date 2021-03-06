# 1. Basic Shapes 

```python
#import required package 
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

```python
#Create various colour dictionary 
colors = {'blue': (255, 0, 0), 'green': (0, 255, 0), 'red': (0, 0, 255), 'yellow': (0, 255, 255),
          'magenta': (255, 0, 255), 'cyan': (255, 255, 0), 'white': (255, 255, 255), 'black': (0, 0, 0),
          'gray': (125, 125, 125), 'rand': np.random.randint(0, high=256, size=(3,)).tolist(),
          'dark_gray': (50, 50, 50), 'light_gray': (220, 220, 220)}

# function for showing images 
def show_with_matplotlib(img, title):
    img_RGB = img[:,:,::-1]
    
    plt.imshow(img_RGB)
    plt.title(title)
    plt.show()
```
```python
#create the canvas to draw: 400 x 400 pixels, 3 channels, uint8 (8-bit unsigned integers)
#set the background to black using np.zeros()
image = np.zeros((400, 400, 3), dtype="uint8")

#we can change the background to our preferred colour 
image[:] = colors['light_gray']
```

## Drawing Lines 
fuction for drawing line - line(img, pt1, pt2, color, thickness=1, lineType=8, shift=0)

```python
cv2.line(image, (0, 0), (400, 400), colors['green'], 3)
cv2.line(image, (0, 400), (400, 0), colors['blue'], 10)

#printing image
show_with_matplotlib(image, 'Basic Line')
```
<p align = "center">
<img src= "https://github.com/professor-4/OpenCV/blob/main/03%20Constructing%20Basic%20Shapes/Output_pic/DrawingLine.JPG" width ="500" height="400" >
</p>

----------------------------------------------------------------------
## Drawing Rectangles 
function for drawing Rectangle is - rectangle(img, pt1, pt2, color, thickness=1, lineType=8, shift=0)

```python
cv2.rectangle(image, (10, 50), (60, 300), colors['green'], 3)
#thickness -1 will fill the full box
cv2.rectangle(image, (80, 50), (130, 300), colors['blue'], -1) 

show_with_matplotlib(image, "Rectangle")
```
<p align = "center">
          <img src= "https://github.com/professor-4/OpenCV/blob/main/03%20Constructing%20Basic%20Shapes/Output_pic/DrawingRectangle.JPG" width ="500" height="400" >
          </p>
          
----------------------------------------------------------------------
## Drawing Circle 
function for drawing circle is - circle(img, center, radius, color, thickness=1, lineType=8, shift=0)

```python
# cv2.circle(image, (50, 50), 40, colors['green'], 3)
# cv2.circle(image, (100, 100), 30, colors['blue'], -1)

show_with_matplotlib(image,'Circle')
```
<p align = "center">
          <img src = "https://github.com/professor-4/OpenCV/blob/main/03%20Constructing%20Basic%20Shapes/Output_pic/DrawingCircle.JPG"  width ="500" height="400" >
          </p>
          
--------------------------------------------------------------------------
















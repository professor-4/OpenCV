# Basic Shapes 

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

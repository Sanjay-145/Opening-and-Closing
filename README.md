# OPENING AND CLOSING

## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Use Opening operation.
### Step 5:
Use Closing Operation.

<br><br><br><br><br>

# PROGRAM:
## Developed by   : P.Sanjay
## Register Number: 212220230042

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'P.SANJAY',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()
```
# Create the structuring element
```
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
```
# Use Opening operation
```
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()
```
# Use Closing Operation
```
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()

```
## OUTPUT:

### Display the input Image

![S1](https://user-images.githubusercontent.com/75235426/170883803-b8e3f1dc-e50e-4187-a56b-6532a330d16f.jpg)

### Display the result of Opening

![s2](https://user-images.githubusercontent.com/75235426/170883817-5c71ad42-8625-4517-8c6e-3d009fa0b34a.jpg)

### Display the result of Closing

![s3](https://user-images.githubusercontent.com/75235426/170883827-c6c21e6f-0752-4a8b-9271-9baad326497a.jpg)

## RESULT:
Thus the Opening and Closing operation is used in the image using python and OpenCV.

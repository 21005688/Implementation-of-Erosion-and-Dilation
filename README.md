# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.


### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
Plot the images using plt.imshow.

 
## Program:
```
Developed by : DEEPIKA.J
Register number : 212221230016

# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," DEEPIKA.J ",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'magma')
plt.axis('off')

# Dilate the image
image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')

```
## Output:


### Display the input Image

![llllllllllll](https://github.com/21005688/Implementation-of-Erosion-and-Dilation/assets/94747031/48ee819d-37f3-4e22-a5c0-361c202456e2)

### Display the Eroded Image
![222222222222](https://github.com/21005688/Implementation-of-Erosion-and-Dilation/assets/94747031/59d3afba-a9d4-45e8-b385-466b3d2ea345)

### Display the Dilated Image
![3333333333](https://github.com/21005688/Implementation-of-Erosion-and-Dilation/assets/94747031/31a3ce3d-635d-4461-a9ca-3825110298e5)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.

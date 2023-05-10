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
## Output:
![llllllllllll](https://github.com/21005688/Implementation-of-Erosion-and-Dilation/assets/94747031/f6779e3a-58fe-47fd-85f8-2eb10f531de7)

### Display the input Image


![222222222222](https://github.com/21005688/Implementation-of-Erosion-and-Dilation/assets/94747031/5cb0ad59-3254-4aeb-ad27-7250d5f65263)


### Display the Dilated Image
![3333333333](https://github.com/21005688/Implementation-of-Erosion-and-Dilation/assets/94747031/41672145-74a0-4de7-a789-b0a864cd732d)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.

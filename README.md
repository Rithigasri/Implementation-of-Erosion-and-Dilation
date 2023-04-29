# EXPERIMENT 10: IMPLEMENTATION OF EROSION ANS DILATION
## AIM:  
To implement Erosion and Dilation using Python and OpenCV.
## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the text image using cv2.putText.
### Step 3:
Then create the structuring image for dilation/erosion.
### Step 4:
Apply erosion and dilation using cv2.erode and cv2.dilate.
### Step 5:
Plot the images using plt.imshow.
## PROGRAM:

``` 
# Import the necessary packages:
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText:
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"Rithiga Sri.B",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')

# Create the structuring element:
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image:
image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'magma')
plt.axis('off')

# Dilate the image:
image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')

```
## OUTPUT:

### Display the input Image:  
![image](https://user-images.githubusercontent.com/93427256/235285185-1ee3c6f8-6c66-40f9-bc6c-716252199a35.png)

### Display the Eroded Image:  
![image](https://user-images.githubusercontent.com/93427256/235285213-955c0fed-102b-44aa-9caa-aef0c70e37c7.png)

### Display the Dilated Image:  
![image](https://user-images.githubusercontent.com/93427256/235285226-a6df276b-71e1-4ec9-9584-9b7b5712e6ee.png)

## RESULT:
Thus the generated text image is eroded and dilated using python and OpenCV.

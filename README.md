# EXPERIMENT 10: IMPLEMENTATION OF EROSION AND DILATION
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
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
img=cv2.cvtColor(text_image,cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(img,"Rithiga Sri.B",(5,70),font,2,(0,0,255),5,cv2.LINE_AA)
cv2.imshow("Original Image",img)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode = cv2.erode(img,kernel)
cv2.imshow("Eroded Image",image_erode)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Dilate the image
image_dilate = cv2.dilate(img,kernel)
cv2.imshow("Dilated Image",image_dilate)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## OUTPUT:

### Display the input Image:  
![image](https://user-images.githubusercontent.com/93427256/235285749-002f73f7-3406-4739-83b9-c3e067dc998e.png)

### Display the Eroded Image:  
![image](https://user-images.githubusercontent.com/93427256/235285775-6c739cc9-147b-4b73-85ff-7e14fed1d3af.png)

### Display the Dilated Image:  
![image](https://user-images.githubusercontent.com/93427256/235285826-c29d2863-9f5a-47f2-b0ab-c5fa5cfb9f5e.png)

## RESULT:
Thus the generated text image is eroded and dilated using python and OpenCV.

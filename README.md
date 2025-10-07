# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step1:
Import the necessary packages

## Step2:
Create the Text using cv2.putText

## Step3:
Create the structuring element

## Step4:
Use Opening operation

## Step5:
Use Closing Operation
 
## Program:

``` Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Hemavathy S', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
```
## Output:

### Display the input Image
<img width="537" height="513" alt="image" src="https://github.com/user-attachments/assets/79754041-1658-4d9a-b418-953699db5095" />

### Display the result of Opening
<img width="536" height="498" alt="image" src="https://github.com/user-attachments/assets/742391af-aecf-4ddf-b0a2-1bf0be51484d" />


### Display the result of Closing
<img width="556" height="509" alt="image" src="https://github.com/user-attachments/assets/e2a70e2c-4e2f-4a23-b0af-d2f339d1ae28" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.

# DIPT-EXP-10
# OPENING--AND-CLOSING

## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
   
## Algorithm:
### Step1:
Import the necessary packages
### Step2:
Give the input text using cv2.putText()
### Step3:
Perform opening operation and display the result
### Step4:
Similarly, perform closing operation and display the result

 
## Program:

# NAME : VARUN JC
# REG NO : 212224240179

``` 
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Hemavathy S', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
```
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
```
```
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
```
# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
```
```
# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
```
```
# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
```
## Output:

### Display the input Image
<img width="472" height="502" alt="image" src="https://github.com/user-attachments/assets/3b109e51-d90b-471c-8278-1be5287bc7a4" />


### Display the result of Opening
<img width="486" height="500" alt="image" src="https://github.com/user-attachments/assets/0a909c6a-7ca1-43e5-bf76-1d46f027ff7a" />


### Display the result of Closing
<img width="482" height="511" alt="image" src="https://github.com/user-attachments/assets/91b8a414-cf17-4c07-9e5b-56c66c6ef820" />


## Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.

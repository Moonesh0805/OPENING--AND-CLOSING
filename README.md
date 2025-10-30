# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
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
DEVELOPES BY: MOONESH P

REG:212223230126

# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'SIVA DINESH',(5,70), font,2,(255),5,cv2.LINE_AA)

```
# Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation

```
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```


# Use Closing Operation
```
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:

### Display the input Image
<br>
<br>
<br><img width="400" height="100" alt="download" src="https://github.com/user-attachments/assets/595b5a0b-494a-4bbf-875f-39e5a7182300" />
<br>
<br>
<br>

### Display the result of Opening
<br>
<br>
<br>
<br><img width="515" height="144" alt="download" src="https://github.com/user-attachments/assets/7ea4953f-caa0-4f6f-9e51-6b7d26cb0f2c" />
<br>
<br>

### Display the result of Closing
<br>
<br>
<br>
<br><img width="515" height="144" alt="download" src="https://github.com/user-attachments/assets/291382e0-4ddf-4546-816e-3c0fbf1f6eee" />
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.

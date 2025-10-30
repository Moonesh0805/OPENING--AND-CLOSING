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
<img width="610" height="178" alt="Screenshot 2025-10-30 153254" src="https://github.com/user-attachments/assets/dab9eb1a-1791-4aab-bcfe-2c2b8cb32971" />


### Display the result of Opening
<img width="822" height="231" alt="Screenshot 2025-10-30 153336" src="https://github.com/user-attachments/assets/cd5ba0bd-9289-410f-975e-84ed864d3f7f" />


### Display the result of Closing
<img width="779" height="222" alt="Screenshot 2025-10-30 153402" src="https://github.com/user-attachments/assets/6ae587c1-30dd-4924-9e04-0f3af7d662f1" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.

# EX 09 Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
#### Step1:<br>
Import the necessary pacakages

#### Step2:<br>
Create the text using cv2.putText

#### Step3:<br>
Create the structuring element

#### Step4:<br>
Erode the image


#### Step5: <br>
Dilate the Image

 
## Program:
```
NAME: DEEPAK RAJ S
REG.NO: 212222240023
```

### Import the necessary packages
``` 
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```
image = np.zeros((300, 600, 3), dtype="uint8")
text = "DEEPAK RAJ S"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)
```
### Create the structuring element
``` 
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```
### Erode the image
``` 
eroded_image = cv2.erode(image, kernel, iterations=1)
plt.subplot(1, 3, 2)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")


```
### Dilate the image
``` 
dilated_image = cv2.dilate(image, kernel, iterations=1)
plt.subplot(1, 3, 3)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")

```

## Output:
### Display the input Image
![image](https://github.com/user-attachments/assets/36f91839-1a43-4f9e-a3fb-23f2c8df0e8c)

### Display the Eroded Image
![image](https://github.com/user-attachments/assets/f9bf41f9-bc47-498b-b6f7-f890e36b4f2c)

### Display the Dilated Image
![image](https://github.com/user-attachments/assets/1837df26-981a-407c-b1aa-5da31118c6ff)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.

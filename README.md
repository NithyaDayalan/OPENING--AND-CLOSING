## OPENING--AND-CLOSING

### Aim :
To implement Opening and Closing using Python and OpenCV.

### Software Required :
1. Anaconda - Python 3.7
2. OpenCV
   
### Algorithm :
#### Step1 :
Create a blank image and add text "NITHYA" using cv2.putText
#### Step2 :
Define a 3x3 kernel as the structuring element
#### Step3 :
Display the input image
#### Step4 :
Apply opening (erosion then dilation) and display the result
#### Step5 :
Apply closing (dilation then erosion) and display the result
 
### Program :

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'NITHYA', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Create the structuring element
kernel = np.ones((3, 3), np.uint8)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
plt.show()

# Use Opening operation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB)) 
plt.title("Opening Operation")
plt.axis('off')

# Use Closing Operation
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB)) 
plt.imshow(closed_image)
plt.axis("off")
```

### Output :
#### Display the input Image :
<img width="486" height="505" alt="image" src="https://github.com/user-attachments/assets/c8e1e77e-01e0-4b71-bef0-da81a91da550" />

#### Display the result of Opening :
<img width="678" height="541" alt="image" src="https://github.com/user-attachments/assets/3164411d-df64-4765-8f68-9d48a621fef5" />

#### Display the result of Closing :
<img width="668" height="513" alt="image" src="https://github.com/user-attachments/assets/9c3a75af-31c6-44e4-afc6-f4f10e39c6cc" />

### Result :
Thus the Opening and Closing operation is used in the image using python and OpenCV.

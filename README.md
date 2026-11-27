# Exp-9--Record-IMPLEMENTATION-OF-EROSION-AND-DILATION
## Implementation of Erosion and Dilation Using OpenCV
## Aim
To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

Image Erosion

Image Dilation

## Software Used
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib

## Algorithm
### Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:
Create a blank image using NumPy.

### Step 3:
Insert text onto the image using OpenCV's text drawing function.

### Step 4:
Display the original image.

### Step 5:
Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion
Apply the erosion operation using the created kernel.
Remove pixels from the boundaries of foreground objects.
Display the eroded image.

### Step 7: Image Dilation
Apply the dilation operation using the same kernel.
Add pixels to the boundaries of foreground objects.
Display the dilated image.

### Step 8:
Compare the original, eroded, and dilated images.

### Program
#### Developed By
#### Name: Divya Dharshini S
#### Register No: 212224240039
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((550, 650, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Divya Dharshini S(212224240039)', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
dilated_image = cv2.dilate(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')

```

## Output

<img width="851" height="706" alt="image" src="https://github.com/user-attachments/assets/cda4bd1b-1b75-4555-adbe-a50f15b0d27b" />

#### Input Image with Text

<img width="873" height="543" alt="image" src="https://github.com/user-attachments/assets/13d2ad24-6314-49b0-9ef5-e7e51d169549" />

#### Eroded Image

<img width="847" height="568" alt="image" src="https://github.com/user-attachments/assets/b4465b64-f8f6-40b1-825a-83f190ea08f6" />

#### Dilated Image

 <img width="817" height="550" alt="image" src="https://github.com/user-attachments/assets/67ebe00f-a1e5-49cd-9a3e-a44d762c73a9" />

## Result
Thus, the morphological operations Erosion and Dilation are successfully implemented using OpenCV.

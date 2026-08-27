# Implementation of Erosion and Dilation Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

* Image Erosion
* Image Dilation

## Software Used

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

## Algorithm

### Step 1

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2

Create a blank image using NumPy.

### Step 3

Insert text onto the image using OpenCV's text drawing function.

### Step 4

Display the original image.

### Step 5

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

* Apply the erosion operation using the created kernel.
* Remove pixels from the boundaries of foreground objects.
* Display the eroded image.

### Step 7: Image Dilation

* Apply the dilation operation using the same kernel.
* Add pixels to the boundaries of foreground objects.
* Display the dilated image.

### Step 8

Compare the original, eroded, and dilated images.

## Program

### Developed By

**Name:** SIVAKARTHIKEYAN
**Register No:** : 212225220098

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Add text to the image
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(
    image,
    'SIVAKARTHIKEYAN',
    (60, 250),
    font,
    1,
    (255, 255, 255),
    2,
    cv2.LINE_AA
)

# Create a 3x3 structuring element
kernel = np.ones((3, 3), np.uint8)

# Apply erosion
eroded_image = cv2.erode(image, kernel, iterations=1)

# Apply dilation
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Display all images
plt.figure(figsize=(15, 5))

plt.subplot(1, 3, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 3, 2)
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis("off")

plt.subplot(1, 3, 3)
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))
plt.title("Dilated Image")
plt.axis("off")

plt.tight_layout()
plt.show()
```

## Output

### Original Image

<img width="356" height="373" alt="image" src="https://github.com/user-attachments/assets/ad10b406-b804-4900-9a84-748f778666f7" />


### Erosion

<img width="367" height="378" alt="image" src="https://github.com/user-attachments/assets/9ddcca5a-0ac4-4859-9a54-76d969debf98" />

### Dilation

<img width="349" height="346" alt="image" src="https://github.com/user-attachments/assets/b4620bc6-6a14-4719-ad1f-910fcc64362d" />


## Result

Thus, the morphological operations **Erosion** and **Dilation** were successfully implemented using OpenCV.

# Implementation of Erosion and Dilation Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.
```
uploaded = files.upload()

image_path = next(iter(uploaded))

img = cv2.imread(image_path)
img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

plt.imshow(img)
plt.title("Original Image")
plt.axis("off")
plt.show()
```

### Step 5:

Create a structuring element (kernel) of suitable size.
```
kernel = np.ones((5, 5), np.uint8)
```

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

```
erosion = cv2.erode(img, kernel, iterations=1)
plt.imshow(erosion)
plt.title("Erosion Image")
plt.axis('off')
plt.show()
```

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.
```
dilation = cv2.dilate(img, kernel, iterations=1)
plt.imshow(dilation)
plt.title("Dilation Image")
plt.axis('off')
plt.show()
```

### Step 8:

Compare the original, eroded, and dilated images.
```
plt.figure(figsize=(15, 5))

plt.subplot(1, 3, 1)
plt.imshow(img)
plt.title("Original Image")
plt.axis('off')

plt.subplot(1, 3, 2)
plt.imshow(erosion)
plt.title("Erosion")
plt.axis('off')

plt.subplot(1, 3, 3)
plt.imshow(dilation)
plt.title("Dilation")
plt.axis('off')

plt.tight_layout()
plt.show()
```

## Program Developed By

**Name:** Sharan Kumar G

**Register No:** 212224230260

## Output

### Original Image

- A text image containing characters is displayed.
- The image serves as the input for morphological processing.

<img width="387" height="515" alt="image" src="https://github.com/user-attachments/assets/b92b6e54-9360-4b62-85ec-cc961633ccbe" />



### Erosion

- Original image is displayed.
- Eroded image is displayed.
- The thickness of the characters is reduced.
- Object boundaries shrink inward.

<img width="407" height="522" alt="image" src="https://github.com/user-attachments/assets/26633979-5d48-4303-93bd-a54e5aed935a" />



### Dilation

- Original image is displayed.
- Dilated image is displayed.
- The thickness of the characters increases.
- Object boundaries expand outward.

<img width="388" height="515" alt="image" src="https://github.com/user-attachments/assets/ecaf74d0-f59d-4241-a848-e1937ac705d2" />



## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.

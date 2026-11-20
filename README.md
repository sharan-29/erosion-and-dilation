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

**Name:** Janesha S

**Register No:** 212225240056

## Output

### Original Image

- A text image containing characters is displayed.
- The image serves as the input for morphological processing.

  <img width="515" height="397" alt="image" src="https://github.com/user-attachments/assets/ec182c4c-f0c4-4955-9ecc-c418677c321d" />


### Erosion

- Original image is displayed.
- Eroded image is displayed.
- The thickness of the characters is reduced.
- Object boundaries shrink inward.

  <img width="515" height="397" alt="image" src="https://github.com/user-attachments/assets/b09cf193-b49b-4adf-9aeb-c8e2e8f367d3" />


### Dilation

- Original image is displayed.
- Dilated image is displayed.
- The thickness of the characters increases.
- Object boundaries expand outward.

<img width="515" height="397" alt="image" src="https://github.com/user-attachments/assets/925cdb36-b223-44a3-922f-20a39c8a751d" />

<img width="1489" height="385" alt="image" src="https://github.com/user-attachments/assets/6f9876ad-0200-4579-b8ee-c1242032c33e" />


## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.

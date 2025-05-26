# THRESHOLDING
## Aim:
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:

### Step1:
Load the necessary packages.

### Step2:
Read the Image and convert to grayscale.

### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.

## Program:

### Name : SRIVATSAN G
### Reg No : 212223230216

### Load the necessary packages

```py
import numpy as np
import matplotlib.pyplot as plt
import cv2
```
### Read the Image and convert to grayscale
```py
image = cv2.imread("cat2.jpg",1)
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
image_gray = cv2.imread("cat2.jpg",0)
```
### Use Global thresholding to segment the image
```py
ret,thresh_img1=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY)
ret,thresh_img2=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY_INV)
ret,thresh_img3=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO)
ret,thresh_img4=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO_INV)
ret,thresh_img5=cv2.threshold(image_gray,100,255,cv2.THRESH_TRUNC)
```
### Use Adaptive thresholding to segment the image
```py
thresh_img7=cv2.adaptiveThreshold(image_gray,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,11,2)
thresh_img8=cv2.adaptiveThreshold(image_gray,255,cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY,11,2)
```
### Use Otsu's method to segment the image 
```py
ret,thresh_img6=cv2.threshold(image_gray,0,255,cv2.THRESH_BINARY+cv2.THRESH_OTSU)
```
### Display the results
#### ORIGIONAL IMAGE
```py


plt.axis("off")
plt.title("Original Image")
plt.imshow(image)

```
![download](https://github.com/user-attachments/assets/2f62a0a8-1c57-4935-8ec9-a40cce3418dd)

#### GREY IMAGE
```py


plt.axis("off")
plt.title("Gray Image")
plt.imshow(cv2.cvtColor(image_gray, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()
```

![download](https://github.com/user-attachments/assets/4b16905e-36c6-438a-adcf-395f0b8870f9)

#### Threshold Image (Binary)
```py


plt.axis("off")
plt.title("Threshold Image (Binary)")
plt.imshow(cv2.cvtColor(thresh_img1, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```

![download](https://github.com/user-attachments/assets/24b3d8c3-b65b-427a-9861-0591ad8c74dd)


#### Threshold Image (Binary Inverse)
```py


plt.axis("off")
plt.title("Threshold Image (Binary Inverse)")
plt.imshow(cv2.cvtColor(thresh_img2, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![download](https://github.com/user-attachments/assets/3e5e0eb3-5e8d-49fd-84ef-b7f1f1afb213)


#### Threshold Image (To Zero)
```py


plt.axis("off")
plt.title("Threshold Image (To Zero)")
plt.imshow(cv2.cvtColor(thresh_img3, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![download](https://github.com/user-attachments/assets/b7c813ce-7f7c-4ad4-8198-5259fc914961)

#### Threshold Image (To Zero-Inverse)
```py


plt.axis("off")
plt.title("Threshold Image (To Zero-Inverse)")
plt.imshow(cv2.cvtColor(thresh_img4, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```

![download](https://github.com/user-attachments/assets/55ab3769-c604-44ed-843d-1eb21087fdd5)

#### Threshold Image (Truncate)
```py

plt.axis("off")
plt.title("Threshold Image (Truncate)")
plt.imshow(cv2.cvtColor(thresh_img5, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![download](https://github.com/user-attachments/assets/ff5a2b6e-4ddd-41af-88b4-511ee9fd7fb0)

#### Otsu
```py
plt.axis("off")
plt.title("Otsu")
plt.imshow(cv2.cvtColor(thresh_img6, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![download](https://github.com/user-attachments/assets/8dba6dfc-b4e0-42e2-92cc-4b2b615b099a)

#### Adaptive Threshold (Mean)
```py

plt.axis("off")
plt.title("Adaptive Threshold (Mean)")
plt.imshow(cv2.cvtColor(thresh_img7, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![download](https://github.com/user-attachments/assets/e6a08793-5f76-45b8-896f-a0c0520289b4)


#### Adaptive Threshold (Gaussian)
```py
plt.axis("off")
plt.title("Adaptive Threshold (Gaussian)")
plt.imshow(cv2.cvtColor(thresh_img8, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![download](https://github.com/user-attachments/assets/e1effc67-e0bc-4b49-a133-2ab5f90bb125)

## Result:
Thus the images are segmented using global thresholding, adaptive thresholding and optimumglobal thresholding using python and OpenCV.

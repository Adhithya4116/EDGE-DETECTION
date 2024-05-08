# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
```py
Developed by: ADHITHYA PERUMAL D
Register Number: 212222230007
```
### Convert image to grayscale and remove noise:
```py
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("spiderman.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)

```
### SOBEL EDGE DETECTOR
### SOBEL X AXIS :
```py
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
### SOBEL Y AXIS :
```py
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
### SOBEL XY AXIS :
```py
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR:
```py
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR:
```py
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR
### SOBEL X AXIS:
![Screenshot 2024-04-10 102303](https://github.com/AbishekAnand15/EDGE-DETECTION/assets/118706942/ef07cfc0-c880-425a-97bb-f8659ba7c171)

### SOBEL Y AXIS:
![Screenshot 2024-04-10 102333](https://github.com/AbishekAnand15/EDGE-DETECTION/assets/118706942/f6dec418-e2f7-4382-9580-242fe1d04736)

### SOBEL XY AXIS:
![Screenshot 2024-04-10 102348](https://github.com/AbishekAnand15/EDGE-DETECTION/assets/118706942/bf3965da-fea9-4c5b-8097-6c4a3d58ea81)

### LAPLACIAN EDGE DETECTOR
![Screenshot 2024-04-10 102356](https://github.com/AbishekAnand15/EDGE-DETECTION/assets/118706942/3895fa15-c003-4ad0-9537-1e0614020f8e)

### CANNY EDGE DETECTOR
![Screenshot 2024-04-10 102407](https://github.com/AbishekAnand15/EDGE-DETECTION/assets/118706942/31210a90-1d14-4804-808d-58a45cb13c7c)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

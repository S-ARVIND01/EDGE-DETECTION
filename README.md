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
```
Developed by : ARVIND S
Register no  : 212222240012
```
### Convert image to grayscale and remove noise:
```python
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("camalion.jpg",0)
gray = cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### Sobel Edge Detector:
#### SOBEL X AXIS: 
```python
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
#### SOBEL Y AXIS:
```python 
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
#### SOBEL XY AXIS: 
```python 
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
### laplacian edge Detector:
```python
laplacian = cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### Canny Edge Detector:
```python 
canny = cv2.Canny(gray,120,150)
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
### SOBEL EDGE DETECTOR :
#### SOBEL X AXIS :
![image](https://github.com/S-ARVIND01/EDGE-DETECTION/assets/118707337/43f7a2f1-b65d-4324-8d10-e4b804a3f027)

#### SOBEL Y AXIS :
![image](https://github.com/S-ARVIND01/EDGE-DETECTION/assets/118707337/de0a1869-20e8-435f-8138-4b41c149858b)

#### SOBEL XY AXIS :
![image](https://github.com/S-ARVIND01/EDGE-DETECTION/assets/118707337/95d651b3-1bd3-4d9b-8bf5-86e391ca822a)

### LAPLACIAN EDGE DETECTOR :
![image](https://github.com/S-ARVIND01/EDGE-DETECTION/assets/118707337/ef8f2c6a-678a-4def-83e8-20bfc862cb21)

### CANNY EDGE DETECTOR :
![image](https://github.com/S-ARVIND01/EDGE-DETECTION/assets/118707337/5e621d7e-37bc-455e-8b78-e44e6a4cb4b7)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

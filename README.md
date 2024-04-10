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
### NAME: RAGAVENDRAN A
### REG.NO:212222230114

## Convert image to grayscale and remove noise
```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("hack.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)

```
## Sobel edge detection:
### Sobel x axis:
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
### Sobel y axis:
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
### Sobel xy axis:
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
## LAPLACIAN EDGE DETECTOR:

```python
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

## CANNY EDGE DETECTOR:

```python
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
# Output:
## Sobel edge detection:
### Sobel x axis:

![Screenshot 2024-04-10 103237](https://github.com/ragavanayyadurai/EDGE-DETECTION/assets/118749557/77a32b43-183b-4e55-abfd-f935337c8968)


### Sobel y axis:

![Screenshot 2024-04-10 103252](https://github.com/ragavanayyadurai/EDGE-DETECTION/assets/118749557/77a504ab-7ec1-40b5-ba87-7d19d06f7a5c)


### Sobel xy axis:
![Screenshot 2024-04-10 103315](https://github.com/ragavanayyadurai/EDGE-DETECTION/assets/118749557/1eb7ad6f-cb58-481d-9e43-f8e0fecc0ded)



## Lapacian Detector:

![Screenshot 2024-04-10 103322](https://github.com/ragavanayyadurai/EDGE-DETECTION/assets/118749557/0668afad-91c0-4af5-9b19-b9ea594ce787)


## Cany edge detector:

![Screenshot 2024-04-10 103330](https://github.com/ragavanayyadurai/EDGE-DETECTION/assets/118749557/aa5c562a-8906-42c8-84aa-e35d4e8682dc)



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

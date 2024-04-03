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
## Program :
### NAME : MAMTHA I
### REG NO : 212222230076
### Convert the image to grayscale:
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("owl.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR :
***SOBEL X AXIS:***
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
***SOBEL Y AXIS:***
```
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
***SOBEL XY AXIS:***
```
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
```
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
```
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
### ORIGINAL IMAGE :
![owl](https://github.com/Mamthaiyappaprabu/EDGE-DETECTION/assets/119393563/70aa1bd3-f000-4322-b5c8-6e7be0c3b2f7)

### SOBEL EDGE DETECTOR :


***SOBEL X AXIS:***


![image](https://github.com/Mamthaiyappaprabu/EDGE-DETECTION/assets/119393563/eeb0c775-b4d1-4822-a1bc-85a4c88d2827)



***SOBEL Y AXIS:***



![image](https://github.com/Mamthaiyappaprabu/EDGE-DETECTION/assets/119393563/e5eb0138-b9b6-42fd-b844-4656d5941de1)




***SOBEL XY AXIS:***


![image](https://github.com/Mamthaiyappaprabu/EDGE-DETECTION/assets/119393563/85aa209b-a50c-4c31-b6b0-55e9a26de72d)






### LAPLACIAN EDGE DETECTOR :

![image](https://github.com/Mamthaiyappaprabu/EDGE-DETECTION/assets/119393563/8d8bc79d-8fd7-49c8-a4ac-31c876113bdb)


### CANNY EDGE DETECTOR :
![image](https://github.com/Mamthaiyappaprabu/EDGE-DETECTION/assets/119393563/d181bcc1-4231-4c21-87cb-b745e2bdb5e7)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

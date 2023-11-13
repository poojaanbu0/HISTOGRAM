# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.<br>


### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.<br>

### Step3:
Display the histograms with their respective images.<br>

### Step4:
Equalize the grayscale image.<br>

### Step5:
Display the grayscale image.<br>

## Program:


#### Developed By: POOJA A
#### Register Number: 212222240072

```python
import cv2
import matplotlib.pyplot as plt
```
## Write your code to find the histogram of gray scale image and color image channels.

### Gray Image
```python
hist = cv2.calcHist([gray_image],[0],None,[256],[0,255])
```
### Color Image 

#### Chanel Blue
```python
h1 = cv2.calcHist([color_image],[0],None,[256],[0,255]) 
```
#### Chanel Green
```python
h2 = cv2.calcHist([color_image],[1],None,[256],[0,255]) 
```
#### Chanel Red
```python
h3 = cv2.calcHist([color_image],[2],None,[256],[0,255]) 
```


## Display the histogram of gray scale image and any one channel histogram from color image


### Gray Image
```python
import cv2
import matplotlib.pyplot as plt
gray_image =cv2.imread('M640.png',0)
cv2.imshow('gray_image',gray_image) 
cv2.waitKey(0) 
cv2.destroyAllWindows()
```
### Color Image
```python
import cv2
import matplotlib.pyplot as plt
color_image =cv2.imread('red_car.png',-1)
cv2.imshow('color_image',color_image) 
cv2.waitKey(0) 
cv2.destroyAllWindows()
```


## Write the code to perform histogram equalization of the image.
```python
equ_img = cv2.equalizeHist(gray_image)
```

# Output:
## Input Grayscale Image and Color Image
![WhatsApp Image 2023-11-14 at 03 01 55_e926f00e](https://github.com/poojaanbu0/HISTOGRAM/assets/119390329/37ff539e-55ec-42e5-a815-536c3440a966)

![WhatsApp Image 2023-11-14 at 03 02 15_3dae67b1](https://github.com/poojaanbu0/HISTOGRAM/assets/119390329/5b93fd18-f348-4e59-9f77-e95b5fc309b9)

## Histogram of Grayscale Image and any channel of Color Image
#### Grey Image
![WhatsApp Image 2023-11-14 at 03 02 34_8ddfbde2](https://github.com/poojaanbu0/HISTOGRAM/assets/119390329/94ff29c3-59fb-42b6-bb66-39c6b21c15c3)

#### Blue Channel
![WhatsApp Image 2023-11-14 at 03 02 54_73c2ceb1](https://github.com/poojaanbu0/HISTOGRAM/assets/119390329/0f9e3278-0f36-4a81-a7b6-b9b5de383c5d)


#### Green Channel
![WhatsApp Image 2023-11-14 at 03 03 26_f7b907c7](https://github.com/poojaanbu0/HISTOGRAM/assets/119390329/cf4b4549-0aa2-4342-b639-ea5df2595332)


#### Red Channel
![WhatsApp Image 2023-11-14 at 03 03 51_6a83695b](https://github.com/poojaanbu0/HISTOGRAM/assets/119390329/b37a9521-7585-45cc-8fa5-ae5631cea11d)


## Histogram Equalization of Grayscale Image
![WhatsApp Image 2023-11-14 at 03 04 37_443916fa](https://github.com/poojaanbu0/HISTOGRAM/assets/119390329/3587914b-ff3c-4e9c-b628-3c3a7adba5a2)


# Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.

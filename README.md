# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the necessary libraries and read two images, Color image and Gray Scale image.
### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.
### Step3:
Display the histograms with their respective images.
### Step4:

Equalize the grayscale image.
### Step5:
Display the grayscale image.

## Program:
```python
# Developed By: harish.g
# Register Number:212220230021



# Write your code to find the histogram of gray scale image and color image channels.

import cv2
import matplotlib.pyplot as plt
Gray_image= cv2.imread('tony.jpg')
re=cv2.resize(Gray_image,(280,175))
Color_image= cv2.imread('ronaldo.jpg') 
cv2.imshow('Gray image',re)

cv2.imshow ('colour image',Color_image)
cv2.waitKey()



# Display the histogram of gray scale image and any one channel histogram from color image

hist  = cv2.calcHist([Gray_image], [0], None, [256], [0,256]) 
histl=cv2.calcHist([Color_image], [1], None, [256], [0,256]) 
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.title("grey image")
plt.show()

plt.stem(histl)
plt.title("color image")
plt.show()

# Write the code to perform histogram equalization of the image. 


Gray_image= cv2.imread('tony.jpg',0)
re=cv2.resize(Gray_image,(280,175))
equ=cv2.equalizeHist(re)
cv2.imshow('Gray Image',re)

cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)






```
## Output:
### Input Grayscale Image and Color Image


![q1](https://user-images.githubusercontent.com/75246297/167475108-92256dbd-1415-4c0f-8e65-106cd08f76e0.jpg)



### Histogram of Grayscale Image and any channel of Color Image


![q2](https://user-images.githubusercontent.com/75246297/167475116-9e3081d3-e910-4d98-8762-dcf2c47b873b.jpg)

### Histogram Equalization of Grayscale Image
![q3](https://user-images.githubusercontent.com/75246297/167475127-31a7ddef-67ce-4a88-b127-7b880561af17.jpg)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.

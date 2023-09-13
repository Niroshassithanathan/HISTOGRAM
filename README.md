# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

## Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

## Step3:
Display the histograms with their respective images.

## Step4:
Equalize the grayscale image.

## Step5:
Display the grayscale image.

## Program:
```
# Developed By:NIROSHA S
# Register Number:212222230097
```
```
import cv2
import matplotlib.pyplot as plt
```
## Write your code to find the histogram of gray scale image and color image channels.
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("cha.jpeg")
color_image = cv2.imread("ch.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Display the histogram of gray scale image and any one channel histogram from color image
```
import numpy as np
import cv2
Gray_image = cv2.imread("cha.jpeg")
Color_image = cv2.imread("ch.jpeg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
cv2.destroyAllWindows()

```
# Write the code to perform histogram equalization of the image. 

```

import cv2
gray_image = cv2.imread("cha.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
![Screenshot from 2023-09-13 13-30-48](https://github.com/Niroshassithanathan/HISTOGRAM/assets/121418437/242d9413-e18c-48ed-898b-5848e5ce4508)

![Screenshot from 2023-09-13 13-53-02](https://github.com/Niroshassithanathan/HISTOGRAM/assets/121418437/34090239-7bb2-4752-b575-0248ecf97de2)

### Histogram of Grayscale Image and any channel of Color Image

![Screenshot from 2023-09-13 14-02-38](https://github.com/Niroshassithanathan/HISTOGRAM/assets/121418437/163bc07a-eabd-4c1b-a069-a5db3e812ef3)
![Screenshot from 2023-09-13 14-02-53](https://github.com/Niroshassithanathan/HISTOGRAM/assets/121418437/499499ac-37e0-4ec5-9e97-455e2e53fcdb)
![Screenshot from 2023-09-13 14-03-04](https://github.com/Niroshassithanathan/HISTOGRAM/assets/121418437/059a495e-fb0a-413c-a2cc-8423ae27028f)
![Screenshot from 2023-09-13 14-03-14](https://github.com/Niroshassithanathan/HISTOGRAM/assets/121418437/d1f39263-2f25-4237-9e8e-1df255b0a487)


### Histogram Equalization of Grayscale Image
![Screenshot from 2023-09-13 13-55-42](https://github.com/Niroshassithanathan/HISTOGRAM/assets/121418437/4c23770c-7980-490b-919e-01492660a1fc)

![Screenshot from 2023-09-13 13-55-59](https://github.com/Niroshassithanathan/HISTOGRAM/assets/121418437/f20945be-028c-47a5-88c9-26a45e89424b)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.

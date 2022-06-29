## Ex no: 4
## Date: 25/04/2022
# <p align="center">Histogram and Histogram Equalization of an image</p>
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
<br>Calculate the Histogram of Gray scale image and each channel of the color image.

### Step3:
<br>Display the histograms with their respective images.

### Step4:
<br>Equalize the grayscale image.

### Step5:
<br>Display the grayscale image.

## Program:
```python
# Developed By: ASHWIN A O 
# Register Number: 212220230005
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('PIC1.jpg')
plt.imshow(Gray_image)
plt.show()
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()


# Display the histogram of gray scale image and any one channel histogram from color image
Color_image=cv2.imread('PIC2.jpg')
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()



# Write the code to perform histogram equalization of the image. 
Gray_image=cv2.imread('LEO_GRAY.jpg',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:
### Input Grayscale Image and Color Image
<br>![1](https://user-images.githubusercontent.com/75234790/167667538-7b023afd-d7f1-4288-9501-72d000b7f33e.jpg)

<br>![,kjhgf](https://user-images.githubusercontent.com/75234790/167667876-b91877ee-834c-4c83-93b9-e80679e981b4.png)

<br>
<br>

### Histogram of Grayscale Image and any channel of Color Image
<br>
<br>![swdefrd](https://user-images.githubusercontent.com/75234790/167667899-7acee126-0af6-4c4a-8896-a1fb3e692674.jpg)

<br>![sadf](https://user-images.githubusercontent.com/75234790/167667926-b0bce88c-c033-45f4-8ba9-967ecfa955c5.jpg)

<br>

### Histogram Equalization of Grayscale Image
<br>
<br>![fdgh](https://user-images.githubusercontent.com/75234790/167667941-6f71fae3-8c2d-4989-97c0-529e03b309f0.png)

<br>
<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.

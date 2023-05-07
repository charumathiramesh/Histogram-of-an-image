# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image

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
# Developed By: charumathi R
# Register Number: 212222240021
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("grayscale.jpg")
plt.imshow(gray_image)
plt.show()
hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Grayscale value')
plt.ylabel('Pixel Count')
plt.stem(hist)
plt.show()




# Display the histogram of gray scale image and any one channel histogram from color image

color_image=cv2.imread("colorimage.jpg")
plt.imshow(color_image)
plt.show()
hist1=cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(hist1)
plt.show()



# Write the code to perform histogram equalization of the image. 

gray_image = cv2.imread('grayscale.jpg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()





```
## Output:
### Input Grayscale Image and Color Image
![1](https://user-images.githubusercontent.com/120204455/236687234-cc50e675-40ab-4228-8aab-2227fe537536.png)


### Histogram of Grayscale Image and any channel of Color Image
![2](https://user-images.githubusercontent.com/120204455/236687257-aa96d3b3-c89b-4a1b-b1a5-5067ee12df31.png)


### Histogram Equalization of Grayscale Image
![5](https://user-images.githubusercontent.com/120204455/236687271-4ebccbbe-4ea2-4e5d-8c42-0eaef0197c93.jpg)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
